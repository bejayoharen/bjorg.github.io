---
layout: single
title:  "Implementing organizational change part 1: culture and policies"
date:   2024-11-07 00:01:00 -0400
categories: management
excerpt: When implementing organizational change, you can influence the culture or implement written policies. What works best when?
---
When implementing organizational change, there are generally two approaches: one is to influence the culture around you to change behavior, and the other is to implement written policies that codify the behaviors you want to see. Let’s talk about why implementing policies, by itself, usually fails, and how to do a better job making changes.

# Why policies alone fail
I have certainly seen leaders, even successful ones, lay down the law with a new policy, initiative or strategy. At times, the worst of these leaders may pretend to listen to feedback, but quickly ignore or dismiss objections. After being on the receiving end of this kind of change a few times, most people start to feel frustrated, either because they don’t fully understand the decision or because they don’t agree with it. Even if they do understand and agree, it can be jarring to have a change like this out of nowhere. When this happens, employees can feel like they’ve been made responsible for results based on someone else’s decision.

Ultimately, the result of this kind of leadership is resentment, feelings of powerlessness and even attrition.

When you have enough authority or charisma, or if you use this strategy sparingly, this kind of leadership _may_ work. However, people who lead by fiat lose a bit of respect (and therefore authority) each time they do so. While there may be situations when you have to lay down the law, I firmly believe it should be the last resort.

# Influencing culture
I was once able to move a company towards a better testing process without any written policies or rules. The company had no policies and while some teams had embraced good testing processes, others were playing it pretty fast and loose. Automated tests existed, but they weren’t implemented consistently and there was no deployment process to ensure they were run before code was put into production. In practice, changes were tested in production, and we occasionally experienced some serious issues.

This was clearly something that needed to change, but I was an IC and didn’t have the authority to implement policy. I was also a new hire, so I hadn’t built much trust yet, so even influencing culture was going to be challenging. One thing I did have going for me, though, was that I was working closely with one of the most influential engineers at the company. He recognized the problem, but hadn’t really mulled it over or prioritized it himself, and didn’t really think it was a big deal. After a few conversations about it in our 1:1s, however, he became an advocate for improved testing. A lot of other folks at the company, under the influence of my colleague, began to prioritize testing as well, and things began to change faster than I expected.

# Policies support culture
As I’ve suggested, implementing policies is, in itself, usually not a good way to change an organization – you need to change the culture first. But good policies can encourage and reinforce good behavior.

In the months after culture started shifting around testing, I was in a position to implement more rigorous CI/CD processes, introduce postmortems, and bring in a new QA company. Making these changes alone might have led to resentment about more paperwork. However, because there was a culture shift towards recognizing the need for better testing, the formalities instead helped to reinforce the culture. People understood that there was a problem and we needed ways to ensure that we maintained our commitment to testing and high-quality releases, so the processes were embraced.

# Involving the team
While simply imposing policies can backfire, there is another way. The trick is to create a new policy _with_ the team. For example, a few years ago my boss and I noticed that larger architecture changes sometimes happened without all stakeholders being properly involved. The solution, to have a proper internal “RCF” process, was obvious enough. But we wanted to make sure everyone was on-board, so we formed a committee to work on it.

My boss and I came to the table with a problem and a goal, but without details of how the process would work. By bringing the problem to a committee, it was much easier to get everyone’s buy-in on the new process. The end result was a process that the team liked because it embodied _their_ values and worked they way _they_ wanted it to.

If you are thinking committees have a natural tendency to slow things down, and therefore it’s not worth forming one, I sympathize. [In my next post](/management/2024/11/06/Implementing-organizational-change-part-2-getting-buy-in.html), I will discuss having a successful committee and how to handle pushback on the changes you want to implement.