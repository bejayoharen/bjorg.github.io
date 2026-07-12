---
layout: single
title:  "Why you haven’t gotten a huge productivity boost from AI (yet)"
date:   2026-07-11 01:01:00 -0400
categories: management
excerpt: And you probably won’t in the near future.
header:
    overlay_image: "/assets/2026/promotion-dark.jpg"
    og_image: "/assets/2026/promotion.jpg"
    teaser: "/assets/2026/promotion.jpg"
---

There’s no doubt that AI has improved the productivity of engineering teams. However, some leaders are expecting change to happen faster. It seems like fully-baked features should be banged out as fast as prototypes, but it still seems to take almost as long as it used to. This doesn’t mean you are doing anything wrong, it just means that AI isn’t magic (at least not yet).

Developers spend most of their time doing things besides writing code. They spend a lot of time figuring out what code they need to write – that's the real challenge of the job – and so far AI hasn’t managed to make that easier. In fact, whenever I have to read a product requirements document or even a linear ticket that was written by AI, I spend more time than I would reviewing a human document, because it’s overly detailed, and harder to distill the important points.

But using AI to make your work easier while making other people’s job harder is [another topic](/slop-at-work). For now, let’s assume AI only helps. Even then, the picture isn’t as rosy as you might think. First, let’s consider a senior developer. Their day might look like this:


|Senior Developer|Pre AI|Post AI|
|---:|:---|:---|
|Writing New Code|1.5|0.5|
|Reading and Debugging|1.5|1.0|
|Design And Architecture|1.0|1.0|
|Code Reviews|0.75|0.75|
|Documentation and Admin|0.75|0.75|
|Testing, CI/CD, deployment|0.5|0.75|
|Mentoring / Pair programming|0.5|0.5|
|Meetings|1.5|1.5|
|**Total**|**8.0**|**6.75**|


So, even if we assume AI makes coding 3x faster (and assuming they spend a bit more on testing, CI/CD and deployment since there’s more new code), A senior developer saves only 1.25 hours per day, or about 15%. FN: we can disagree about the specific numbers here, but if you think this is wildly off, you’ve probably never been a Senior Engineer.

Now let’s consider a junior developer:

|Junior Developer|Pre AI|Post AI|
|---:|:---|:---|
|Writing New Code|2.75|1.0|
|Reading and Debugging|1.5|1.0|
|Design And Architecture|0|0|
|Code Reviews|0.5|0.5|
|Documentation and Admin|0.5|0.5|
|Testing, CI/CD, deployment|0.75|1|
|Learning / Pair programming|1.0|1.0|
|Meetings|1.0|1.0|
|**Total**|**8.0**|**6**|


AI makes this junior developer about 25% more efficient. This is a bigger difference than for the senior developer because they spend more time coding, which is the part of the job AI boosts the most.

It’s ironic that I still hear leaders saying things like, “we only hire senior engineers because AI does the work of juniors”, when it’s juniors who stand to gain the most from AI – especially if they are good at using AI as a learning tool, not just an overeager side-kick who’s willing to do the menial work.[^pipeline]

If the above observations surprise you, or you think developers spend more time than this actually writing code, you probably haven’t ever been a senior developer, and don’t understand the true complexity of the job.[^doorman] Think about the interview process: would you hire someone you knew was a good coder, but you knew nothing about their ability to reason about systems with others, or to break down vague requirements into tangible action items? I wouldn’t, and that’s why I interview for those skills, rather than just coding skills.

# Notes

[^pipeline]: Andrew Murphy writes more about misguided "[VPs who went to a conference and came back saying 'AI does junior work now' like they'd just discovered fire.](https://andrewmurphy.io/blog/ai-didnt-kill-your-junior-pipeline-you-did)

[^doorman]: You've probably never been a [doorman](https://en.wikipedia.org/wiki/Doorman_fallacy) either.


