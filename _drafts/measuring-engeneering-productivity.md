---
layout: single
title:  "The hazards of measuring engineering productivity"
categories: management
date: 2025-03-12 01:01:00 -0400
excerpt: Productivity is hard to measure, but worth thinking about.
header:
    overlay_image: "/assets/2025/productivity-dark.jpg"
    og_image: "/assets/2025/productivity.jpg"
    teaser: "/assets/2025/productivity.jpg"
---

There’s a lot being written these days about measuring engineering performance and productivity. Some of the confusion, I believe, stems from conflating performance and productivity. In this post, I’ll define and discuss productivity, and save performance for a future article.

By definition, productivity is rate of output per unit of input. In engineering, input is usually time and money, though often enough the vast majority of the money is engineer’s salaries, so we sometimes only think of one or the other. Output is a bit more complex – we’d like to measure how much value is added to a company’s product offering, but that can be quite nebulous.

# Why productivity is hard to measure

It’s tempting to believe that one of the most technical and measurement-obsessed fields should easily be able to measure its own productivity. Sales can do it, so why not engineering? The problem mostly comes down to not knowing how much value is added to a company’s bottom line for any given piece of engineering work.

<figure>
    <img
		 src="/assets/2025/productivity.gif"
         alt="Animated GIF of a graph of multiple things which broadly move together, but have many small ripples that don't match up.">
</figure>

In some cases, we can measure business impact. For example, Meta can measure the value of a new product by running an AB test and measuring how much additional engagement the feature creates, which they know how to translate into dollars. By dividing by the amount of time spent on the new product, they can establish a reasonable estimate of productivity.

However, not every company or product team can do the kind of analysis Meta can do, and even Meta is limited in where and when it can apply this analysis. For example, a lot of work engineering does is hard to attribute to a specific project: all that work your team does to ensure smooth deployments can benefit many projects. Meta may be able to amortize those costs over time and across many projects if they wanted, but for the rest of us, the detailed analysis is probably not worth it.

For many companies, especially small startups and scaleups, it’s often not clear what the dollar value of a project is. While most tech companies (hopefully) have some product providing value for customers and income for the company, most companies also have products and features which have more subtle impact on the business, like creating a press moment.

Even for a product where you can do the necessary measurements, there’s still a problem with this kind of analysis: the numbers you need to do the calculations aren’t usually available until after the project is done, so the best you’ve got is a lagging indicator of productivity. These kinds of productivity numbers are often way too late to be of any use to a small startup with 18 months of runway.

# What can we measure?

Given the above, you might think I’m advocating against trying to measure team performance in any way. That’s not the case – in fact, I think as organizations grow it becomes increasingly more important – more about that in my next post – and I also think it can be useful to think about productivity when planning projects, even if you don't have the numbers yet.

# Why productivity is still a useful thing to think about

<figure>
    <img
		 src="/assets/2025/expensive.gif"
         alt="Animated GIF of seth meyers speaking. The caption reads ELEVEN GAZILLION DOLLARS">
    <figcaption>It's always worth considering the cost.</figcaption>
</figure>

Ultimately, you always have to be asking yourself if you are working on the most impactful project at any given time, and even if you don’t have clear numbers, productivity can be a useful lens for guiding you to the right decisions.

For example, I once worked at a company that developed a fancy landing page for a new product. After the fact, I did a little back of the envelope math and determined that, after considering developer time, designer time and product management time, the project cost well into the hundreds of thousands of dollars. The company might have felt the initiative was worth it, but would they have made the same choice if they had a cost and time estimate before they started? Did it really bring in hundreds of thousands of dollars worth of value over simply using off-the-shelf software like squarespace?

My guess is that it was not worth it. After presenting my analysis to stakeholders, the next time they wanted to build a custom landing page, they went straight to wix, so I take it they agreed.
