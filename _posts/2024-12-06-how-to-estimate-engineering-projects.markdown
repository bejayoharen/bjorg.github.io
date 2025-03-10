---
layout: single
title:  "How to estimate engineering projects"
date:   2024-12-06 01:01:00 -0400
categories: management
excerpt: Engineers often need to estimate their work, but doing so can be a challenge.
header:
    overlay_image: "/assets/images/estimating-dark.png"
    og_image: "/assets/images/estimating.png"
    teaser: "/assets/images/estimating.png"
---
I learned to estimate projects as a contractor, where sticking to my hours and timeline could mean the difference between getting repeat business and never hearing from a client again. I got good at it very quickly.

Even if you are working at a company that is fairly forgiving about inaccurate timelines, creating accurate estimates is a great way to build trust in your abilities, and is a skill that can help to make planning, such as roadmapping more accurate and more useful.

## Step 0: Gather as much information as you can

The more information you have about the project (requirements, stakeholders, scale, etc), the easier it is to estimate. Early on in the planning stages you will likely have the least information, and you might have to make some assumptions. For example, I’ve been asked to estimate a project with little more than a title and a vague sentence or two from the CEO about what’s desired. In cases like that, it’s usually understood that your estimate is going to be more of a guestimate, but it might still be useful to the organization, eg in deciding which projects are worth pursuing in a given year.

The minimum thing you need to understand is what the minimum requirements for the stakeholders or the business are. The better you understand that, the more you'll be able to determine what actually needs to be built.

That said, you should always do your best to get whatever information you can. For information you can’t get, I advise you to couch your estimates in terms like, “assuming we just have to do A, I think this will take two weeks, but if we have to do X, Y, or Z it could take considerably longer and I’d need more information about those requirements.”

Always be prepared to revise your estimate as you go and more information comes in.

## Step 1: Create a gut-check by thinking of a similar project.

The first real step in estimating is to create a gut-check by thinking about a similar project you did in the past. If the projects are similar enough, you should be able to get a reasonable baseline that you can use to check a more detailed analysis. Ideally, you’d put some thought into how the project you are estimating is different from the past project and how that will impact your timeline. For example, if your new project is for a new client, uses a more complex technology or has a dependency on a team you haven’t worked with, it might take longer.

The more experience you have as an engineer with different kinds of projects, the easier and more accurate your gut-checks will become. However, even if you are just getting started it’s helpful to do your best here. Remember the goal isn’t to use this as an estimate, but to provide a baseline for comparison to gut-check your more detailed work.

## Step 2: Break the project down into the smallest tasks you can.

You might be tempted to stop at step 1. If you are pressed for time, and just need a rough estimate, that might be good enough. However, you can achieve more accurate results by breaking down the project into individual tasks.

The more you can break down your project into smaller tasks the more accurate your estimates will be. The less experienced you are, the smaller the tasks should be because you’ll have less experience estimating big tasks. Done properly, thinking about each task also reveals dependencies, and helps remind you of all the things that need to get done.

Once the project is broken into smaller tasks, estimate each task by comparing it to the last time you did something similar. It’s more important to include all the tasks than to accurately estimate each task. This is because small errors in estimates tend to cancel each other out, while leaving tasks out will always result in an underestimate.

Because we are talking about estimating time, I encourage you not to use story points, which measure complexity and don’t have much meaning outside an individual team. Instead we want to estimate time. For example, on a small project I’m doing myself, I might estimate how many hours each task will take. If on the other hand, I’m estimating a big project for a team to do, I might estimate in weeks.

## Step 3: Identify unknowns and estimate the process of resolving them.

The more unknowns (aka “open questions”) there are, the harder it is to make an estimate. Unknowns can include technology (such as libraries) you’ve never used before, dependencies on other teams, ability of existing technology to handle a new task, and so on.

Unfortunately, unless the project is trivial or a tremendous amount of time is set aside for estimating, you usually won’t be able to resolve all unknowns. The best strategy is to make a guess and then put the tasks needed to answer open questions first on your timeline. By doing so, you'll be able to go back and refine your estimate sooner rather than later. If your assumptions turned out to be wrong, discovering that quickly maximizes the time you have to take that information into account.

Another advantage of having assumption-checking be first on the timeline is that it signals to your stakeholders that you take the timeline seriously, which helps to build trust. Stakeholders often worry that timelines aren’t taken seriously by development teams, so putting assumption-checking first signals that you know the timelines matter. It also gives you and your stakeholders the information you need to make decisions before a lot of time and money is wasted.

I learned this lesson on a contract project I did years ago. I was confident a problem a client had could be solved with Java in a web browser (This was back in the day when a JVM was standard in browsers), but they were not confident because they’d never heard of something so complex being done in an “applet” as they were called. The concern was reasonable, so we agreed to build a demonstration first. A little time making a demo gave them the confidence to know they were minimizing risks, and when my demo worked out, it gave them confidence to invest more in the technology.

## Step 4: List potential complexities like dependencies that might slow you down.

The more people involved and the more other kinds of complexity there are, the harder it is to get a good estimate. Especially challenging is if people are going to be involved in other projects at the same time, and you can’t guarantee their quick turnaround when you need them to contribute. It’s helpful if the philosophy of the team is to prioritize dependencies, but if that’s out of your control, you might just need to make some reasonable assumptions about how much these sorts of things can slow you down.

If I’m working as a contractor, I make it clear what kinds of things might slow me down. If I’m working as part of a team, I’m always sure to track down dependencies and figure out how it’s going to impact what I do. In terms of actual calculations, it’s tricky to know how much to change your estimates based on this, but what I usually do is try to figure out a percentage of my project that’s going to be spent coordinating, waiting and generally agonizing and add that percentage to the total.

## Step 5: Pad your estimate.

When you take all the above and add it together you will have a reasonable estimate. However, mistakes in estimating tend to represent forgotten tasks, unexpected difficulties and hiccups, rather than tasks that were easier than you expected, so the project is unlikely to go faster than you estimated but it might go a lot longer.

That’s why the final (and most dubious) step in estimating is to pad it. How much you pad is a question of experience and judgement. At this point, the work you do in step 1 to compare to a similar project is especially useful as a guide. If your baseline project took 2 weeks and your estimate is for 1 week, It probably makes sense to lean on the baseline estimate. If on the other hand, they both came out to 2 weeks, you probably don’t need much padding.