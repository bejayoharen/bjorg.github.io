---
layout: single
title:  "Engineering performance metrics"
categories: management
date: 2025-03-12 01:01:00 -0400
excerpt: Measuring performance is more practical than measuring productivity, and can have diagnostic benefits as well. Although it can be complex, starting simple can have a big impact.
header:
    overlay_image: "/assets/2025/performance-dark.jpg"
    og_image: "/assets/2025/performance.jpg"
    teaser: "/assets/2025/performance.jpg"
---

While [measuring productivity](link to last article) can be hazardous, measuring and tracking measurement of one specific areas of engineering, such as speed of deployment, can be very useful. I'm calling such measurements "performance metrics".

The best performance metrics give us data about things that contribute directly to productivity, which allows us to at least hope that by improving performance, productivity will go up as well. A small collection of the right performance metrics can replace trying to measure productivity.

# Selecting metrics for your team

<figure>
    <img
		 src="/assets/2025/connected.gif"
         alt="Animated GIF of a grizzled man in front of a wall of pictures connected in complex ways via yarn. The caption reads: Everything on this wall is connected.">
    <figcaption>Don't let complexity stop you from getting started.</figcaption>
</figure>

There are a million trendy engineering metrics you can use (many of which are described below and in linked articles), but ultimately, the right ones will depend on your situation. I recommend starting small, and just picking a few metrics so you aren't overwhelmed with data.

Selecting the right metrics for your situation may involve some judgement calls. If you are just getting started, I think it’s okay to start with some ad-hoc guestimates rather than trying to come up with detailed measurements for everything right off the bat. For example, instead of measuring how long it takes to deploy a new release or get feedback on a PR, you might just ask your engineers if any of them find it to be a problem. If they say no, it’s likely not worth focusing your efforts there.

# Continuous improvement metrics

If you are looking to improve the output of your team, here are some metrics that can be useful to track continuously. You may focus on one or two for a time, but you should be keeping an eye on a number of these.

<figure>
    <img
		 src="/assets/2025/allshine.gif"
         alt="Animated GIF of moira Rose from Schitt's Creek speaking. The caption reads: when one of shines, all of us shine">
</figure>

* **Frequency of deployments**. If your team is deploying frequently, it’s an indicator that they have confidence in the entire machinery around what matters most: delivering value to customers. If deployment frequency is low, it may indicate problems with testing, CI/CD, or PR process. You probably need to do further diagnostics into each of those steps. Some metrics that contribute to this include: Time to Deploy, Frequency of merges/commits, and time to respond to PRs.
* **Incident recovery time**. If it takes a long time to handle an incident, not only does that mean your team is spending too much time fixing bugs, but it also erodes customer confidence in your team and product.
* **Frequency of incidents**. If incidents are happening too often, it’s time to stop and figure out why. Is code not being properly tested? Are PR reviews not thorough enough?
* **Roadmap stability**. Knowing how often (and by how much) your teams are changing their roadmaps can tell you how much your teams are churning. While some roadmap changes are inevitable – especially at very early stage companies – too many changes can indicate your team lacks clarity on their goals, and isn’t able to push the company forward as effectively as possible because they are too frequently spending time churning.
* **Number of AB tests run**. Knowing how often your team is validating assumptions can be especially useful for larger, and consumer-facing brands. Pushing forward with new features without testing them regularly can be a sign that people are working, but not necessarily on the most impactful thing. Smaller companies with limited resources should at least do before/after tests to confirm that they are improving software and not just adding bells and whistles that their customers don’t need or want.[^1]
* **Team satisfaction**. It should go without saying that a happy team is a productive team, but not every company measures satisfaction of their teams or does anything about it. Team surveys are a great tool that can give excellent qualitative and quantitative data. If you aren’t sure where to start, I would start here – your team might just be able to tell you what other things are and are not going well.[^sat]

For each of these, remember not to punish or single out individuals. If there’s a problem, it’s your problem as an engineering manager to fix. Using these metrics to punish (or praise) teams and individuals over each other can lead to gaming of the metrics (making them useless) and loss of trust. Moreover, it's important to understand if the metrics apply differently to different teams 

# Diagnostic Metrics
Sometimes you are able to identify a problem with your continuous improvement metrics, but need more data to figure out what’s really going on and how to fix it. Sometimes it will be obvious, but sometimes you need other metrics to help figure out the root problem. Here are some that I find useful.

<figure>
    <img
		 src="/assets/2025/let-it-out.gif"
         alt="Animated GIF of man in glasses on a couch. Caption reads: Tell me all your PROBLEMS. LET IT ALL OUT.">
</figure>

* **Tickets completed**. Looking at how many tickets an individual team completes in a sprint is useful because it can indicate how the team is breaking down its work. Are the chunks too big and therefore poorly estimated? Are they too small and represent so little work that it doesn’t add value?
* **Code Churn**. If code is rewritten or reworked frequently it’s a sign that your team lacks clear direction from the beginning. Some churn is a natural result of feedback and healthy rethinking, but too much may indicate a problem with team processes.
* **Perception of productivity**. I like to ask around outside of engineering and see what people think. If people feel engineering is not doing a good job, it might be true, and they might have insight as to why. It might also indicate a communication problem. Either way it needs to be corrected, and sometimes people who work closely with (but not inside of) engineering can have insights.
* **Lead time**. If it takes too long to go from ticket to delivery, your team is probably overwhelmed. It may be time to reprioritize, and face the reality that not everything in the backlog can get done.
* **Work in progress**. If the number of tickets “in progress” or otherwise not “done” per engineer is too high, it’s a sign that developers may be spending too much time switching between tasks or stuck on blockers. Most blockers should be handled without management intervention, but if not, you may have a problem with team structure, poor planning, or a disempowered team.
* **Code test coverage**. I go back and forth on how useful test coverage actually is. After all, it matters less how much code is tested and more which code is tested. Still, low code test coverage, especially in paths that deal with critical data, is not a good sign.

This is not a list that I think is perfect for all companies, but I think this is a good start for most mid-sized companies.

Some things I left out on purpose are Velocity and Lines of Code because they can be harmful. For example, velocity is sometimes used to compare teams, something it’s neither intended for, nor capable of doing. Lines of Code can be a useful in very broad strokes to gauge overall work levels, but it’s been abused in the past as a way of measuring productivity, or comparing individuals.

# Links

* [A new way to measure developer productivity -- from the creators of DORA and SPACE](https://newsletter.pragmaticengineer.com/p/developer-productivity-a-new-framework)
* [Using metrics to measure individual performance](https://lauratacho.com/blog/using-metrics-to-measure-individual-developer-performance)
* [Four key metrics](https://www.thoughtworks.com/en-de/radar/techniques/four-key-metrics)
* [Dora](https://dora.dev/)
* [Software engineering culture metrics](https://davidxiang.com/2021/02/10/software-engineering-culture-metrics/)
* [Primer on engineering delivery metrics](https://leaddev.com/software-quality/primer-engineering-delivery-metrics)
* [Tying engineering metrics to business metrics](https://icchasethi.medium.com/tying-engineering-metrics-to-business-metrics-f4df7651e026)
* [The best product engineering org in the world](https://www.jamesshore.com/v2/blog/2025/the-best-product-engineering-org-in-the-world)
* [Core 4](https://www.lennysnewsletter.com/p/introducing-core-4-the-best-way-to)

# Footnotes

[^1] : I'll probably write more about this in the future, but criteria for testing should be determined in advance, and should generally represent a greater increase than merely "statistically significant". This prevents you from cluttering your UI with features that individually made some improvement, but together cause customers to feel overwhelmed. Plus, each feature needs to be supported and that can lead to a lot of work that isn't worth it. Choosing your criteria in advance also prevents you from digging through your data to find some metric which improved -- [which is nearly always possible](https://en.wikipedia.org/wiki/Multiple_comparisons_problem). For example, you may decide in advance that you will move forward with a new feature only if it achieves >10% engagement after a two week test.
[^sat] : Satisfaction is measured via a survey. I love running surveys because they can be a quick and surprisingly accurate way to collect data about the engineering team. They reveal not just how the team is feeling, but, if you also ask the right questions, what the problems are and where you need to focus your attention.
