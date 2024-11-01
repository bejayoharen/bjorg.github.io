---
layout: post
title:  "The myth of microservice isolation"
date:   2024-11-01 12:01:00 -0400
categories: management
---

In the last twenty years, microservice architecture (MA) has become the standard way of building web-scale software systems, to the point that architecture conversations usually start not with should we use MA, but rather which specific microservice pattern to use.

I’m not disputing the advantages of MAs, particularly for large tech companies and scale-ups, but I am concerned that companies are making the transition from monolith to microservice without considering all of the challenges that naturally come with the territory. There has been some acknowledgement of the downsides of microservice architecture, including the increased complexity of deployment, tracing, testing, and security, but there’s one downside that I think doesn’t get enough attention: MAs, especially when not guided by clear principles, don’t provide isolation in a way that makes sense to the business.

# The myth of isolation

The idea that microservices are loosely coupled, and therefore easier to update and change in isolation is true to a point, but the conclusion that teams working with microservices can work more independently to ship new features is false. In practice, the isolation created by microservices doesn’t always align with the business: end-user features can seldom be created by making a change to one microservice alone. Microservices are isolated in the sense of deployment, database access and other technological measures, but typically not by end-user feature, and this can mean that microservices are more fragmented, rather than more isolated.

The problem is made worse by another touted benefit of microservices: the idea that each service can be written using the best technology for that service. At huge companies where enormous scale often requires fine-tuned performance and careful alignment of technology to the problem domain, this is a benefit. However, at a smaller or mid-sized company it is usually more important to be able to build features quickly. In this case, even simple changes to multiple services require expertise from people in a variety of technologies, and sometimes from a variety of teams, which automatically expands the scope of the original feature request. With multiple teams involved, coordinating priorities and schedules.

One startup I worked at had gone down the path of using multiple technologies. In some ways, this was good: high-throughput and data-intensive systems could be run in a language suited to that purpose (Scala), while a structured web application could be written in a language suited to that purpose (Python/Django). Unfortunately, adding a new feature to the web often required support from downstream backend services. Since Scala is a fairly challenging language, it was difficult for Python developers to make even relatively simple-seeming changes, and they were therefore forced to ask another team for help.

Of course there’s nothing wrong with teams helping each other, but when different teams have different KPIs, timelines and priorities, cross-team collaboration always adds overhead. This is one of the reasons larger companies with many loosely-coupled systems move more slowly.

# Don't ignore the problem

I’m not suggesting going back to a monolith is necessarily the right answer, but the problem can’t be ignored, either. Here are some tools I used to mitigate the increased scope caused my multiple services and technologies:

1. Careful consideration of dependencies in planning. Dependencies must be anticipated so that downstream teams can be sure to allocate the resources necessary. Asking one team to drop what they are doing and work on something else is a formula for frustration and stalled projects. Making evaluation of these dependencies a part of the planning process makes all the difference.
2. Structure teams with these challenges in mind. You don’t always have the luxury of staffing every team with someone who can work on each technology, but when you do, you can turn a dependency involving considerable amounts of work into a dependency involving just a PR review. This is a night and day difference in getting a product out the door quickly. Related options include creating temporary teams, or pools of resources that can be borrowed as needed. [more about team structure](/management/2024/10/23/structuring-product-engineering-teams.html)
3. Training. It’s possible to get everyone (or at least a critical mass) trained up on all the core technologies used by the company, and some companies do invest in this. At the Scala/Python company, really getting everyone up to speed on multiple languages would have required a significant investment, especially since Scala is not an easy language to master. Since we were usually able to solve the problem with team organization, training did not become a core part of my solution, but we did create opportunities for people who wanted to pursue this route themselves.

You might wonder if I considered undoing the MA transition entirely or finding some way to reduce the technological fragmentation. The truth is that the downsides, while challenging, were tractable and the upsides were significant: it’s hard to imagine how the company could have scaled without the transition. With 20/20 hindsight, however, I do think it’s possible to say that a narrower strategy aimed at fewer and more accessible technologies, and using Scala only where there was a particular strong argument for it, would have made the company as a whole more flexible and improved velocity.