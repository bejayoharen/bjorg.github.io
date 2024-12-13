---
layout: single
title:  "Engineering team growth part 3: Structuring interviews"
date:   2024-12-13 01:01:00 -0400
categories: management
excerpt: Properly structuring interviews helps ensure an unbiased, accurate assessment.
header:
    overlay_image: "/assets/images/team-growth-1-dark.png"
    og_image: "/assets/images/team-growth-1.png"
    teaser: "/assets/images/team-growth-1.png"
---
*This is part three in a [series on Engineering team growth](/series/engineering-team-growth/). Although a lot of info in this post stands on its own, you may want to read [part 1](/management/engineering-team-growth-1-job-description/) first, where I explain how to write a good job description, and then [part 2](/management/engineering-team-growth-2-interview-panel/), where I explain how to prep the interview panel.*

# Interview basics

The goal of interviewing someone is to determine if they will be a productive member of your team. Productivity should include more than the work they contribute directly, and include adding to the team’s knowledge, morale, and ability to function. It’s no good hiring someone who lacks coding skills, but it’s also no good hiring someone who needs to be micromanaged because they can’t prioritize tasks or someone who off-puttingly whines about every task and brings the whole team down.

To assess all this in a short amount of time is hard, and I’m not sure the perfect interview strategy exists to always filter out the problem candidates and always identify the shining stars. However, for all the cries of “tech interviews are broken”, sticking to research-based, tried and true interview techniques actually works fairly well, especially if you understand how and why they work, but the process is still quite difficult and imperfect – we all know that great engineer who made it through 8 rounds and somehow didn’t get the job.

[Joel Spolsky emphasizes just two things](https://www.amazon.com/Smart-Gets-Things-Done-Technical/dp/1590598385?ie=UTF8&s=books&qid=1181076229&sr=8-1) you need to identify in a candidate: 1. They are smart, and 2. They can get things done. If you can identify candidates that meet these criteria, he says, it’s likely a good hire. While I agree with him, I’ve seen problems with how people interpret “smart” to mean whatever *they* think of as smart. For example, many big tech companies consider you smart because of where you got your degree or your ability to solve abstract problems.

A UC Berkley grad who can accurately estimate the number of pennies that fit inside the statue of liberty and rigorously prove that the big O performance of all operations of a red black tree is O(long n) is certainly smart. But I prefer to think in terms of finding someone who can do the job. To do this, I go through each requirement on the JD and find a way to test it. For example, if the job involves coding in Python, I ask the candidate to write some code in Python. If it involves dealing with a complex codebase, I give them a complex codebase and see if they can deal with it. If it involves collaborating with stakeholders, I give them a sample scenario with stakeholders and ask how they’d handle it.

In any given interview, you can likely only check one or two items from the JD, so you should work with your panel to decide who is responsible for testing each skill. Once you know what skill you are testing for, you should come up with a technical question or assessment to determine the candidate’s abilities.

You’ll also want to take some time to dig into their experience, but it’s important to realize the limitations of asking questions about the past. Questions starting with “tell me about a time when…” and “how do you approach…” are easily prepared for and easily lied about. It’s much more telling to present a hypothetical scenario and see how they handle it. Eg “imagine you are on a team with a full roadmap and already behind on your timeline. Now a stakeholder asks to add new features to one of the projects. How would you address that stakeholder?”

Finally, you’ll want to make sure you are conveying information to the candidate, not just getting information from them. Be sure to sell them on your place of work. This is your best opportunity to influence them to take the job if they receive an offer, and that they feel good about the company even if you don't extend an offer. I had a nice interview at DuoLingo and even though I decided the position wasn't a good fit before the interviews finished, I left feeling great about the company and even wanting to other engineers to them.

# Sample interview structure

Let’s look at a good way to conduct your interview. Here's a basic outline you can't go wrong with:

* Introductions (10 minutes)
* Resume Questions (10 minutes)
* Technical Question(s) (30 minutes)
* Questions (10 minutes)

You’ll notice this adds up to a full hour. Trying to shorten interviews might save you a few minutes, but it’s unlikely you’ll do a good assessment in 30 or 45 minutes. If you think you can, you probably aren’t asking a hard enough technical question.

Let’s break these sections down.

# Introductions

You’ll want to spend a few minutes letting the candidate get comfortable. Interviewing is stressful and if you give them a few minutes to get comfortable with you, they will perform better. I like to take a moment to say:

* who I am.
* how long I’ve been at the company and what I’ve done there.
* what my job is, how it relates to the position being hired for, and how we might work together.
* what I like about my job and the company.
* what the rest of the interview is going to look like.

# Resume Questions

Notice this section is not called “resume review”. While it might seem nice to let the candidate tell their story, their story should be clear to you already from having read their resume in advance. Moreover, abdicating control of the interview allows the candidate to give you their rehearsed highlight reel. Focus on questions or concerns *you* have about their resume.

So, instead of the "walk me through your resume" routine, take these ten minutes to ask specific questions about specific items on the resume that popped out at you. This gives you a chance to see if they are able to communicate about the work they did in simple language, and find out if there the major accomplishments listed on their resume really represented their work and not their teammate's. I like to pick a previous job and ask these questions:

* “How did the company make money, and how did you contribute to the company’s revenue or to reducing costs?” You want to make sure you are hiring someone who understands how their work matters to the bottom line, and can communicate their impact in clear language.
* “Who was on your team?” Follow this up by asking about everyone’s role on the team to understand what they really were (and were not) responsible for.
* “What was your role in [some accomplishment]?” Dig in enough to find out if the accomplishments on the resume were inflated, or perhaps actually done by someone else.
* “What were some of the challenges you faced in [some accomplishment]?” This will give you a real sense of how they operate and deal with pushback, or if others were, in fact, dealing with those thorny problems.

# Technical Question(s)

This is the real meat of the interview and should be focused on a core job responsibility like coding or system design. Your job is to ask a question that provides a reasonable proxy to something they do on the job. The better the proxy, the better an indicator you’ll get about the person’s performance on the job.

## Coding questions
Leet and whiteboard coding questions are one type of proxy used in interviews, but these questions are more correlated to how much someone prepared for the job interviewing process or how recently they studied data structures and algorithms than how productive they are going to be at work.

Depending on the job, a better proxy might be showing them some out of date code and asking them to identify issues and fix them. Another idea is to give them a takehome where they build something working, and discuss how they solved the problem in an interview. Some companies give very complex takehomes which I think unfairly and unhelpfully weeds out people who are already employed or otherwise can’t commit to 20 hours of building something for a job they aren’t even sure they want yet. On the other hand, these kinds of projects are excellent proxies for the job.

## Systems Questions
Like traditional coding questions, I’m not sure traditional systems design questions are the best proxy for day to day work. Most engineers will never need to design an entire system with a dozen microservices from scratch, but they will need to navigate existing, imperfect systems, and understand how they communicate with each other.

I prefer to ask questions that get to the heart of those challenges. For example:

> Imagine you have built a system to compete with google search. Imagine you already have a crawler and a way to store the crawled information, but you need to build the part where people can actually come and search for the info they want. As an absolute minimum starting point, what endpoints would you need to implement? [^1]

I make sure they give me:
* exact URLs and HTTP verbs.
* detailed description of what data is included in each request and response.
* how the data is formatted and exchanged (eg, as JSON in the body, in query parameters, etc).

I follow up a question like that with a question about scaling to see if they understand the basics of load balancing and horizontal vs vertical scaling.

## Prioritization
Engineers need to understand which tasks are most critical, and they need to be able to break down a complex task into smaller tasks that deliver value incrementally. I like to give them a wireframe design or just have them go to a website of a product they are likely familiar with and ask how they would break down development and delivery of the product.

When properly done, this is a great proxy for the kind of work they need to do every day: make decisions about what to work on next and understand what has the most value to the company.

This is a great interview for a product manager to do, because it’s exactly the kind of work they will do with a product manager. Successfully completing this question involves collaboration, communicating with non-engineers as well as making the right decisions.

## Other questions
While I think coding, systems, and prioritization are the core parts of most technical interviews, there are other questions you might want to ask depending on the job requirements. Don’t be afraid to think outside the box a little.

Regardless of what question you ask, always make sure you are asking questions where you know what a good answer looks like. If you are asking a new question, always run it by a colleague first and see if they answer the way you expected.

It’s not uncommon, for any type of question, for an interviewee to need to ask clarifying questions, get a little hint, or confirm their understanding of something. This is an opportunity for you to assess their communication and collaboration skills, but you should also have a firm understanding of what constitutes too much help.

# Questions

Always leave a few minutes at the end of the interview for them to ask questions. This is a good chance to put your best foot forward for the company and sell the candidate on the best parts of the job. You want to make sure candidates leave the interview feeling good about the company.

Some people evaluate the candidate asks to see if they prove, through their questions, that they’ve done their research, are sufficiently prepared, or exhibit curiosity. Personally I don’t do this. I’m not going to judge someone who needs to rest their brains a bit between interview sessions.

# Post interview

When the interview is over, your work is not done. It’s important to make an independent assessment of the candidate's performance. The best way to do this is right after the interview, using a rubric you devised ahead of time. I recommend writing your assessment before talking to anyone else, so your thoughts aren't colored by other people's opinions.

Hopefully the hiring manager for the role has given you a form or document to fill out, but if not, here’s what I like to jot down after every interview:

* Did the candidate complete the challenge successfully? (1-5 + notes on where they did especially well or had particular challenges)
* Did the candidate have the right experience for the job? (1-5 + notes)
* Did they communicate clearly throughout the process? (1-5 + notes on where they did especially well or had particular challenges)
* Did they express empathy? (1-5 + notes. eg did they think about how others might react to a problem, did they think through what made the most sense for users, etc)
* Did they exhibit any red flags? (eg nasty comments about old coworkers)
* Do you recommend hiring? (yes or no. If you are on the fence, that’s a no)

# Footnotes

[^1]: I don’t actually ask about Google because this problem only needs two simple endpoints (one to return the home page and one to return the search results. Both are GET requests with HTML responses), but you get the idea. Another question you could ask might be about a system built as a monolith, and a new feature needs to be added. "Do you build it into the monolith or as a new service?" Or "given this complex existing monolith, what part might you break out into a microservice first?" These kinds of things are much more common real-world scenarios than building a system with 15 microservices all coming into being at once.