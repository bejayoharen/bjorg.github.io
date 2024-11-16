---
layout: post
title:  "Frequency detection using the FFT (aka pitch tracking) With Source Code"
date:   2024-11-17 12:01:00 -0400
categories: audio
---
Years ago I noticed that there were a lot of questions on stack overflow about how to track pitch with the FFT. I wrote this post on my old blog along with [a complete, working example](https://github.com/bejayoharen/guitartuner). That code is not the best tool for the job, but it's illustrative of the technique and easy to follow.

Using the FFT is not actually the best pitch tracking method available for tracking or detecting pitch of an audio signal. While it is possible to make a good pitch tracker using the FFT, doing it right requires more work than I do here. The algorithm shown here works, and works reasonably well, but if you need something that converges on the correct pitch really quickly, is very accurate, or tracks multiple notes simultaneously, you need something else.

<figure style="display: block;
  margin-left: auto;
  margin-right: auto;
  max-width: 100%;
  max-width:  400px;
  height: auto; text-align: center;">
    <img style="max-width:  400px; margin: auto;" 
		 src="/assets/images/pitch-tracking-fft.gif"
         alt="It's not necessarily as simple a it seems to find the pitch from an FFT. Some pre-processing is required as well as some knowledge of how the data is organized.">
    <figcaption>It's not necessarily as simple as it seems to find the pitch from an FFT. Some pre-processing is required as well as some knowledge of how the data is organized. In this figure, the fundamental frequency is close to 50 Hz, but the largest peak is around 120 Hz.</figcaption>
</figure>

This code compiles and runs on Mac OS X and Ubuntu Linux and you should be able to get it to run on other platforms without much trouble. If you want to port to other languages, that shouldn't be too hard either.

# The Big Picture

To do our pitch detection, we basically loop on the following steps:

* Read a chunk of audio sample data
* Low-pass the data
* Apply a window to the data
* Transform the data using the FFT
* Find the peak value in the transformed data
* Compute the peak frequency from the index of the peak value in the transformed data

This is the main processing loop for the tuner, with some stuff left out:

    while( running )
    {
        // read some data
        err = Pa_ReadStream( stream, data, FFT_SIZE );

        // low-pass
        for( int j=0; j<FFT_SIZE; ++j ) {
          data[j] = processSecondOrderFilter( data[j], mem1, a, b );
          data[j] = processSecondOrderFilter( data[j], mem2, a, b );
        }
        // window
        applyWindow( window, data, FFT_SIZE );

        // do the fft
        for( int j=0; j<FFT_SIZE; ++j )
          datai[j] = 0;
        applyfft( fft, data, datai, false );

        // find the peak
        float maxVal = -1;
        int maxIndex = -1;
        for( int j=0; j<FFT_SIZE; ++j ) {
          float v = data[j] * data[j] + datai[j] * datai[j] ;
          if( v > maxVal ) {
              maxVal = v;
              maxIndex = j;
          }
        }
        float freq = freqTable[maxIndex];
        //...
    }

Let's go over each of the steps and see how they work.

# Audio Data

We always need to start with a sequence of numbers representing the amplitude of audio over time (sometimes called "Linear, PCM audio"). This is what we get from most uncompressed audio formats like AIFF and WAV. Its also what you get from audio APIs like ASIO, CoreAudio and ALSA. In this case, we are using PortAudio, which acts like a portable wrapper around these and other APIs. If you have a compressed format such as MP3 or OGG, you will have to convert it to uncompressed audio first.

Your data might be 16-bit integer, 8-bit integer, 32-bit floating point or any number of other formats. I'll assume you know how to get your data to floating point representation in the range from -1 to 1. PortAudio takes care of this for us when we specify these input parameters:

    inputParameters.device = Pa_GetDefaultInputDevice();
    inputParameters.channelCount = 1;
    inputParameters.sampleFormat = paFloat32;
    inputParameters.suggestedLatency = Pa_GetDeviceInfo( inputParameters.device )->defaultHighInputLatency ;
    inputParameters.hostApiSpecificStreamInfo = NULL;


You'll also need to know how often your audio is sampled. For a tuner, less is more, so we'll use a sample rate of 8 kHz, which is available on most hardware. This is extremely low for most audio applications (44.1 kHz is considered standard for audio and 48 kHz is standard for video), but for a tuner, 8 kHhz is plenty.

    #define SAMPLE_RATE (8000)

# Low-Pass Filtering

There's no hard and fast rule about low-pass filtering (or simply "low-passing") your audio data. In fact, it's not even strictly necessary, but doing so can get rid of unwanted noise and the higher frequencies that sometimes masquerade as the fundamental frequency. This is important because some instruments have component frequencies called harmonics that are more powerful than the "fundamental" frequency, and usually we are interested in the fundamental frequency. Filtering, therefore, can improve the reliability of the rest of the pitch tracker significantly. Without filtering, some noise might appear to be the dominant pitch, or, more likely, the dominant pitch might appear to be a harmonic of the actual fundamental frequency.

A good choice for the filter is a low-pass filter with a center frequency around or a little above the highest pitch you expect to detect. For a guitar tuner, this might be the high E string, or about 330 Hz. So that's what we'll use -- in fact, we low-pass it twice. If you are modifying the code for another purpose, you can set the center frequency to something that makes sense for your application.

If you aren't sure about the highest frequency or want something less aggressive, you could try a moving average filter, which simply outputs the average of the current input and some number of previous inputs. Intuitively, we can understand that this filter reduces high frequencies because signals that change quickly get "smoothed" out.

    // Process every sample of your input with this function
    // (this is not used in our guitar tuner)
    function float twoPointMovingAverageFilter( float input ) {
      static float lastInput = 0;
      float output = ( input + lastInput ) / 2 ;
      lastInput = input;
      return output;
    }

The moving average filter won't make a huge difference, but if the low pass filter I used in my code doesn't suit you and you don't have the required knowledge of DSP to design the right digital filter (or don't know what the right filter is), it might be better than nothing. I haven't tested the moving average filter with the tuner myself.

# Windowing

Generally speaking, FFTs work in chunks of data, but your input is a long or even continuous stream. To fit this round peg into that square hole, you need to break off chunks of your input, and process the chunks. However, doing so without proper treatment may prove detrimental to your results. In rough terms, the problem is that the edges get lopped off very sloppily, creating artifacts at frequencies that aren't actually present in your signal. These artifacts, called "sidelobes", cause problems for many applications. I know that some tuners are designed without special treatment, so you can skip this step, but I strongly recommend you keep reading because it's easy to deal with this problem.

To reduce the sidelobes, we premultiply each chunk of audio with another signal called a window, or window function. Two simple and popular choices for window functions are the Hamming window, and the Hann window. I put code for both in the tuner, but I used the Hann window.

    void buildHanWindow( float *window, int size )
    {
      for( int i = 0 to size )
          window[i] = .5 * ( 1 - cos( 2 * M_PI * i / (size-1.0) ) );
    }
    void applyWindow( float *window, float *data, int size )
    {
      for( int i = 0 to size )
          data[i] *= window[i] ;
    }

For a tuning app, the windows may overlap, or there may be gaps in between them, depending on your needs and your available processing power. For example, by overlapping and performing more FFTs, and then averaging the results, you may get more accurate results more quickly, at the cost of more CPU time. I strongly recommend doing this in real apps. I did not do this in my app to make the code easier to follow, and you'll see that the values sometimes jump around and don't respond smoothly.

# FFT
The FFT, or Fast Fourier Transform, is an algorithm for quickly computing the frequencies that comprise a given signal. By quickly, we mean O( N log N ). This is way faster than the O( N2) which how long the Fourier transform took before the "fast" algorithm was worked out, but still not linear, so you are going to have to be mindful of performance when you use it. Because the FFT is now the standard way to compute the Fourier transform, many people often use the terms interchangeably, even though this is not strictly correct.

The FFT works on a chunk of samples at a time. You don't get more or less data out of a Fourier Transform than you put into it, you just get it in another form. That means that if you put ten audio samples in you get ten data-points out. The difference is that these ten data points now represent energy at different frequencies instead of energy at different times, and since our data uses real numbers, and not complex, the FFT will contain some redundancies -- specifically, only the first half of the spectrum contains relevant data. That means that for ten samples in, we really only get five relevant data-points out.

Clearly, the more frequency resolution you need, the more time data you need to give it. However, at some point you will run into the problem of not being able to return results quickly enough, either because you are waiting for more input, or because it takes too long to process. Choosing the right size FFT is critical: too big and you consume lots of CPU and delay getting a response, too small and your results lack resolution.

How do we know how big our FFT should be? You can determine the accuracy of your FFT with this simple formula:

    binSize = sampleRate/N ;

For example, with a bin size of 8192 (most implementations of the FFT work best with powers of 2), and a sample rate of 44100, you can expect to get results that are accurate to within about 5.38 Hz. Not great for a tuner, but, hey, that's why we are sampling at 8000 Hz, which gives us an accuracy of better than 1 Hz. Still not perfect, for, say, a 5 string bass, but you can always use a a larger N if you need to. Keep in mind that getting enough samples to get that much accuracy takes longer than a second, so our display only updates about once a second. That's yet another reason you might want to overlap your windows.

The output of the FFT is an array of N complex numbers. It is possible to use both the real and imaginary part to get more accurate frequency information, but for now we'll settle for something simpler and much easier to understand: we simply look at the magnitude. To find the magnitude of each frequency component, we use the distance formula:

    for( i in 0 to N/2 )
      magnitude[i] = sqrt( real[i]*real[i] + cmpx[i]*cmpx[i] );

Now that we know the magnitude of each FFT bin, finding the frequency is simply a matter of finding the bin with the maximum magnitude. The frequency will then be the bin number times the bin size, which we computed earlier. Note that we don't actually need to compute the square root to find the maximum magnitude, so our actual code skips that step.

# More
We do a bit more in our code, like identify the nearest semi-tone and find the difference between the that semi-tone and the identified frequency, but for stuff like that I'll leave the code to speak for itself.