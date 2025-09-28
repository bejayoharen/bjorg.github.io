---
layout: single
title:  "The hazards of measuring engineering productivity"
categories: management
date: 2025-09-12 01:01:00 -0400
excerpt: Productivity is hard to measure, but worth thinking about.
header:
    overlay_image: "/assets/2025/productivity-dark.jpg"
    og_image: "/assets/2025/productivity.jpg"
    teaser: "/assets/2025/productivity.jpg"
---

There’s a lot being written these days about measuring engineering productivity, with some people insisting you [can measure it](https://jellyfish.co/library/engineering-productivity/), and [others insisting you can't](https://www.reddit.com/r/EngineeringManagers/comments/1f51ibl/engineering_productivity_metrics_tools_that_you/).

I think most of the disagreement stems from different definitions of the term productivity. Going by a strict definition, productivity can not be measured in any meaningful way. There are proxies for productivity which can be measured and these are sometimes called "engineering productivity metrics", but strictly speaking they aren't measuring productivity. I'll talk about them in a future article.

# Why productivity is hard to measure

By definition, productivity is rate of output per unit of input. In engineering, input is usually time and money. Often enough, the vast majority of the money is engineering salaries, so we can simplify by just considering time. Output, though, is more complex – we’d like to measure how much value is added to a company’s product offering, but that can be quite nebulous.

<figure>
    <img
		 src="/assets/2025/productivity.gif"
         alt="Animated GIF of a graph of multiple things which broadly move together, but have many small ripples that don't match up.">
</figure>

In some cases, we *can* measure business impact. For example, Meta can measure the value of a new product by running an AB test and measuring how much additional engagement the feature creates. By dividing by the amount of time spent on the new product, by the dollar value of the additional engagement, they can establish a reasonable estimate of productivity.

However, not every company or product team can do the kind of analysis Meta can do, and even Meta is limited in where and when it can apply this analysis. For example, a lot of work engineering does is hard to attribute to a specific project: all that work your team does to ensure smooth deployments can benefit many projects. Meta may be able to amortize those costs over time and across many projects if they wanted, but even for them, the detailed analysis is probably not worth it.

For many companies, especially small startups and scaleups, it’s often not clear what the dollar value of a project is. While most tech companies (hopefully) have some product providing value for customers and income for the company, most companies also have products and features which have more subtle impact on the business, like creating a press moment, or appeasing a high value customer.

Even for a product where you can do the necessary measurements, there’s another problem with this kind of analysis: the numbers you need to do the calculations aren’t usually available until some time after the project is done, so the best you’ve got is a lagging indicator of productivity. These kinds of productivity numbers are often way too late to be of any use to a small startup with 18 months of runway.

Given the above, you might think I’m advocating against trying to measure team performance in any way. That’s not the case – in fact, I think as organizations grow it becomes increasingly more important – more about that in my next post – and I also think it can be useful to think about productivity when planning projects, even if you don't have the numbers yet.

# Why productivity is still a useful thing to think about

<figure>
    <img
		 src="/assets/2025/expensive.gif"
         alt="Animated GIF of seth meyers speaking. The caption reads ELEVEN GAZILLION DOLLARS">
    <figcaption>It's always worth considering the cost.</figcaption>
</figure>

Ultimately, you always have to be asking yourself if you are working on the most impactful project at any given time, and even if you don’t have clear numbers, productivity can be a useful lens for guiding you to the right decisions. You also need to understand if your process is as efficient at developing valuable features as it could be, and there are god metrics for measuring parts of that process.

For example, I once worked at a company that developed a fancy landing page for a new product. After the fact, I did a little back of the envelope math and determined that, after considering developer time, designer time and product management time, the project cost well into the hundreds of thousands of dollars. The company might have felt the initiative was worth it, but would they have made the same choice if they had a cost and time estimate before they started? Did it really bring in hundreds of thousands of dollars worth of value over simply using off-the-shelf software like squarespace? My guess is no.

After mentioning the costs to stakeholders, the next time they wanted to build a custom landing page, they used wix instead of having it custom built, so I take it they agreed.
