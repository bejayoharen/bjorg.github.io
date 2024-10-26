---
layout: page
title:  "Topics"
permalink: /topics/
---

I wasn't sure if I had enough to say to write a blog, so I brainstormed some ideas, and it seems I do. Here are some things I plan to cover at some point or other. Topics here are organized conceptually. Please reach out and let me know if some of these seem especially interesting, and I'll prioritize them:

* Audio
	* Audio Basics
		* [Sampling and digital audio basics](/audio/2024/10/23/digital-audio-basics-sampling-analog-and-digital-conversion.html)
		* [Audio timing source](/audio/2024/10/23/audio-clocking-and-audio-video-synchronization.html)
		* Audio file formats
		* Conversion from float to int and dithering.
		* Decibels
		* Metering audio and audio overviews
		* Choosing bit depths
	* Effects and processing
		* Developing an Intuition for Filtering
		* Implementing biquad filters
		* Orfanidis correction
		* Other considerations for iir filters (recalculating parameters)
		* Interpolating
			* Linear interpolation
			* Exponential/log interpolation
		* Time-delay based effects: echo/delay, flange/chorus, reverb.
		* Filter based effects: phaser
		* Dynamics effects: Compression, limiting
		* Distortion effects: clipping
	* The Frequency Domain
		* Why are sine waves fundamental to audio
		* Frequency vs time domain basics
		* Frequency vs time domain — why we usually go with time domain. Why inverse FFT FIR filters don’t work.
		* Pitch tracking with the FFT
	* Practical considerations:
		* Processing in chunks/chunk sizes
		* Latency
		* Responding to realtime parameter changes and automation
		* Edit artifacts
		* Cross-fading
	* Misc
		* De-esser
		* Rta
		* Phase meter
* Engineering Management
	* A Roadmapping System that Works
	* Regular Manager Meetings
	* [Structuring Product and Engineering Teams](/management/2024/10/23/structuring-product-engineering-teams.html)
	* We need a new way to point stories.
	* Keeping Remote Teams on track
	* The Agony of Dependencies
	* Some Microservices should be libraries
	* What is Strategy in Management and Engineering?
	* Influencing culture vs implementing policies (why not both?)
	* Accountability, team charters and buy-in
* Contracting
	* How I got work as an audio software development contractor
	* How to Estimate Projects
	* How to set your rates
