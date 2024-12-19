---
layout: single
title:  "Engineering team growth part 7: Dealing with a growing organization"
date:   2024-12-19 01:01:00 -0400
categories: management
excerpt: Bringing in more employees lets your company get more done, but it also comes with additional challenges you must prepare for.
header:
    overlay_image: "/assets/images/team-growth-1-dark.png"
    og_image: "/assets/images/team-growth-1.png"
    teaser: "/assets/images/team-growth-1.png"
---

*This is part seven in a [series on Engineering team growth](/series/engineering-team-growth/).*

If it’s time to grow your team, you are about to face a number of challenges. Hiring, onboarding and training is time-consuming, meaning your team is going to be less productive. Once you’ve hired, you still aren’t done because your now larger team is going to require additional organizational structure, and possibly new infrastructure.

# Before you hire

Before you start hiring, make sure everyone in the organization is ready to invest the time needed to do a good job at this critical task. This means hiring managers and people on interview panels need to understand that hiring will slow them down. They may have to communicate downstream about any impacts to timelines. That applies to other folks involved as well, such as people responsible for onboarding, training, and sourcing.

In the short term, growing your team will slow you down. It’s worth doing some back of the envelope math to figure out how much your planned growth will slow your velocity, and make sure that everyone’s comfortable with that.

You might do the math and find the results unacceptable, especially if you are trying to grow your department by large amounts, eg 50% in eighteen months. You might be tempted to see if you can lower the burden of hiring on your current staff so the short term impact is lower. While making your processes as streamlined as possible is a noble goal, don’t sacrifice the quality of your hiring process. If you do, the process will leave you with a company full of people you shouldn’t have hired, and that’s not worth the relatively small gains you can make in the short term.[^1]

# Required org changes for growth

As you grow, you typically start to need more layers of management. In a perfect world, you can grow existing people into new roles, but in practice you don’t always have someone ready for a promotion when you need it. That means you need to hire more managers when you hire more ICs.

For startups hiring their first full-time people manager, this can feel very uncomfortable. A common reaction is, “but there’s so much to do, can we really afford to be hiring managers right now?” These startups often have a hard time hiring because they aren’t really sure what management of an engineering team entails and how hiring an engineering manager can benefit them.

I once interviewed for a position at a company facing this challenge. They knew they needed a manager when they confessed to me that they thought their engineering team was not being as productive as it could be, They estimated that they could get a sixty percent increase in productivity out of their existing team with the right manager, but they were unwilling to consider hiring someone who wasn’t going to spend most of their time writing code, so they were trying to find a candidate who was both an exceptional developer and exceptional manager. Such unicorns exist, but most people reach a point where they can’t competently do both and continue to grow their career, so they tend not to exist for long.

I doubt they found their unicorn, and eventually had to make a choice, which I see as this: they could either boost the productivity of their team by 60% or add 1 IC. Boosting their team's productivity by 60% was the equivalent of adding 7 ICs. The unicorn is unlikely to be as effective at boosting team productivity, so if they did find a unicorn, they probably ended up somewhere in the middle: 3.5 ICs added by productivity, and .5 IC added by the manager themselves. Not bad, and they'd probably see that as win, even if they could do better.

I realize that is all pretty arm-wavy -- who knows if they could really get 60% additional productivity by hiring a manger. But the fact is, they believed they could and still didn't want to hire a manager.[^2]

# Infrastructure

Deploying to EC2 with a script that copies code and config files from local machines might be fine if you just have a few people and a non-mission critical service. However, as you get more people, all trying to deploy multiple times a day (or at least multiple times a week), you need infrastructure to manage all those deployments properly. Unfortunately, getting all this working is still a full-time job at many companies. Technologies like Heroku can ease the burden, but as you start to scale they become increasingly expensive. Other technologies, like Vercel, may not work with your stack.

Technologies like Kubernetes, are becoming increasingly popular for growth-scale companies, but it people to manage them. At some point, through some combination of startups and open-source technology I hope this becomes a solved problem, but for now, be prepared to invest in people to build and maintain your infrastructure.

# Footnotes

[^1]: At the same time, don't over-engineer your hiring process. [Adding more complexity and more approvals may not mean better hires, but it will mean more burden.](https://hbr.org/2022/07/its-time-to-streamline-the-hiring-process).

[^2]: For the same reason, managers are often the first to go in layoffs, leaving existing managers to take on more reports. Organizations can and do muddle through with too few managers, but teams get less productive over time. This is especially true of good managers, who drive not just projects, but culture and process, so that when they are gone, the culture and processes they cultivated continue for some time on inertia.