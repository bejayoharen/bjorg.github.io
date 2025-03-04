---
layout: single
title:  "Improving product roadmapping"
date:   2025-01-30 01:01:00 -0400
categories: management
excerpt: A good roadmapping process supports the company’s strategy and helps focus the company’s efforts. Here's how to make it easier to accomplish those goals.
header:
    overlay_image: "/assets/2025/roadmapping-dark.jpg"
    og_image: "/assets/2025/roadmapping.jpg"
    teaser: "/assets/2025/roadmapping.jpg"
---
*This is a case study of how I improved the roadmapping process at a company where I was VP Engineering. In future posts, I plan to dig in more to the requirements and process of roadmapping at any mid-sized companies, as well as how to get buy-in for changes like these.*

A major goal of roadmapping is to ensure that every team is focusing the limited number of working hours they have on the most impactful projects throughout the coming months (or years). However, the chaos and rush that often characterizes the process can make it easy for everyone to lose sight of that goal, no matter how clearly it is presented by leadership. A structured, step-by-step process can help enforce the goals, clarify the process and achieve better results.

# Diagnosing the problem

Not to long ago, I was working at a company that took roadmapping to the extreme: every year was like starting over with new high-level objectives, initiatives and strategy. Old roadmaps were thrown out and new ones were made with the new goals in mind. We were still a mid-stage startup, so it made sense to rethink goals and roadmaps as milestones were reached and new ones came on the horizon.

However, the roadmapping process was painful for many people, and I heard many complaints in casual conversation. While these hallway complaints weren’t particularly actionable, there was enough general frustration that I decided to dig in and see if I could make some improvements. With surveys and 1:1 meetings I uncovered a few themes:
1. Some team leaders were unsure about what level of certainty was expected, or how that level of certainty should be achieved.
2. Some team leaders felt the accuracy of their roadmaps was not very good, and that it was impossible to improve in the time allotted. Therefore, they reasoned, roadmapping was futile.
3. Some team leads viewed roadmaps as a tool to impress leadership with their ambition, or get signoff on their plans, rather than a process that might actually yield results they could use themselves.
4. Most teams lacked a clear framework for evaluating and selecting projects. Many teams were unclear on who was responsible for determining level of effort and how the team would decide which projects to take on.

It was clear that the existing process was not accomplishing one of its main goals: forcing teams to decide what they were – and were not – going to accomplish.

# Updated process

To resolve these issues, I created a standardized process for each team to follow. For each step, I also made it clear what the desired outcome was, and who was responsible for it. The first year we implemented this, I allowed teams to opt out, but most teams were eager to try something new, especially since I had designed the process with their feedback.

Here was the process:

1. The product owner compiles a list of all potential projects. This includes input from stakeholders, leadership, and the team itself.
2. The product owner meets with stakeholders and establishes the core requirements for each project and prioritizes each item.
3. The engineering lead estimates how long each project will take, based on the core requirements. For each project, they think about a similar project from the past, and enter into a spreadsheet how many weeks and how many engineers are needed.
4. Together, the engineering lead and the product owner decide which projects they will – and will not – commit to. The spreadsheet has a checkbox for each project that lets them try different scenarios and see how close any given combination of commitments would bring them to their overall team capacity. I encouraged teams to select enough projects to get to 50-75% of their total capacity to leave room for emergent issues, dependencies and so on.
5. The product owner takes the committed projects and puts them on a timeline.
6. Engineering leads from all teams meet to ensure dependencies are taken into account and all teams can commit to the downstream work they need to do.

For te teams, the new process clarified the roles and responsibilities of the product owner and the engineering lead, and the most important outcome, which was a commitment to a set of projects.

Just as important, the process clarified the purpose of the exercise: rather than a tool to impress superiors with ambition, or get sign-off, the true purpose of the exercise was to make sure the team could focus their limited resources on the most impactful projects. Some teams got the message right away.

For other teams, there was still a struggle: I received more than one completed spreadsheet where the teams were clearly over capacity. When I flatly refused to sign-off on these roadmaps, it was a hard lesson for the teams who were avoiding the hard work of scoping down, saying no to less important projects, and investigating alternative solutions.

# Measuring the results

By comparing the accuracy of the roadmaps made by teams that used the new process and those that opted out, we we able to determine how well the new process worked. In terms of overall number of projects completed and accuracy of timelines, the new process did over 20% better.[^1]

Perhaps more importantly, teams were much happier. Through surveys, 1:1s and [retros](https://www.atlassian.com/agile/scrum/retrospectives), I found that even engineers who were skeptical of process (and especially process with spreadsheet-enforced steps) appreciated the change. The feedback suggested that having clear steps helped everyone work together better and get better results with less frustration. Several survey respondents specifically called out that they appreciated knowing who was responsible for what in each step of the process.

An advantage of the new process for leadership was having a consistent way to review everyone’s roadmaps and evaluate their decision-making process. Even with 12 teams to review, it was easy for me to have a good sense of which teams would actually get done the projects they committed to, and quickly determine if there were projects that I needed to dig in on.

After the first year, we decided to roll out the new process to all teams.

# Continued improvements

Since the first major change, we continued to track and implement tweaks to the process every year. For example, in the initial spreadsheets, I included a step where teams would identify any possible dependencies. Because dependencies inevitably slow down projects, the spreadsheet included an automatic update to the level of effort calculation. While including this correction was a smart move overall, the built-in calculation didn’t do a good job of estimating how much they slowed projects down, which frustrated some teams. This was easy to tweak.

# Notes

[^1]: there is admittedly some bias in the sample here since the teams themselves decided whether they wanted to follow the new process or not, but I think if we were to redo this with random sampling we’d get similar results.