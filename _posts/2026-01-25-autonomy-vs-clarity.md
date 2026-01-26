---
layout: single
title:  "Autonomy and Clarity in Leadership Styles"
date:   2026-01-25 01:01:00 -0400
categories: management
excerpt: There's no one right style of leadership. Use the right style of at the right time.
header:
    overlay_image: "/assets/2026/autonomy-vs-clarity-dark.jpeg"
    og_image: "/assets/2026/autonomy-vs-clarity.jpeg"
    teaser: "/assets/2026/autonomy-vs-clarity.jpeg"
---

Over the years I've gone back and forth about the right approach to management and leadership -- should you give your team autonomy and trust to develop solutions themselves, or should you give them specific objectives and direct the team in a hands-on way? Should you come to the table with a strong point of view and get as much buy-in as you can, or build consensus by working with all stakeholders to come up with a plan together?

Mulling these questions over eventually led me to the obvious conclusion: a good leader has a toolkit of different approaches and knows which to apply when. There are a number of factors in deciding the right approach, such as how much autonomy each approach allows the team to have, and how much clarity it gives them about what they need to do.

<div style="margin: 1em auto; text-align: center; max-width:900px;" class="mermaid">
---
title: Leadership Styles
config:
    theme: neutral
    quadrantChart:
    themeVariables:
        quadrant1Fill: "#ddd"
        quadrant2Fill: "#ddd"
        quadrant3Fill: "#ddd"
        quadrant4Fill: "#ddd"
        quadrantInternalBorderStrokeFill: "#aaa"
        quadrantExternalBorderStrokeFill: "#aaaaaa"
---
quadrantChart
    x-axis Low Autonomy --> High Autonomy
    y-axis Low Clarity --> High Clarity
    By Autonomy:::dot: [0.9, 0.2] radius: 2, color:#000000
    By Involvement:::dot: [0.4, 0.8] radius: 10, color:#aa0000
    By Conviction:::dot: [0.15, 0.95] radius: 12, color:#ff0000
    By Policy:::dot: [0.6, 0.6] radius: 2, color:#000000
    By Consensus:::dot: [0.7, 0.7] radius: 4, color:#ff0000
    classDef dot stroke-color:#000000, stroke-width: 0px
</div>

_Figure 1. Different leadership styles have different trade-offs. In this diagram, size indicates amount of context required (larger is more), and color indicates the amount of coordination the problem requires (red is more). This chart is obviously very hand-wavy, but I think it can be helpful to visualize which approaches are suited to which problems._

<div style="margin: 1em auto; text-align: center; max-width:900px;" class="mermaid">
---
title: Leadership Style Decision Tree
config:
    theme: neutral
---
flowchart TB
    a(Is Central Coordination Needed?)
    b(Is it possible for you to gather and understand the full context?)
    d(Do you plan to gather the full context yourself?)
    c(Is it a repeated decision?)
    Policy(Policy)
    Involvement(Involvement)
    Conviction(Conviction)
    Consensus(Consensus)
    Autonomy(Autonomy)
    b -- yes --> d
    b -- no --> Involvement
    d -- yes --> Conviction
    d -- no --> Consensus
    a -- yes --> b
    a -- no --> c
    c -- yes --> Policy
    c -- no --> Autonomy
</div>

_Figure 2. A decision tree can help decide which leadership style to use when. There are other ways to break this down, but this is a good start._

# Leadership by autonomy

### What it is
There are as many leadership styles as there are leaders, but many of the most talked about styles can be grouped under "leadership by autonomy" because they all emphasize trusting teams to figure out how to achieve them. That is, they function by trusting in teams and individuals to carry out work autonomously.

A popular tool among leaders who emphasize this style is the [inverted org chart](https://www.organice.app/blog/inverted-org-chart-when-to-use-and-how-to-make-it). This is used as a visual signal to remind people that the [leaders are servants](https://en.wikipedia.org/wiki/Servant_leadership) of the ICs and that the ICs have the most context and are best positioned to make decisions. Personally, I think inverting the org chart is more useful as a gimmick to get people thinking differently about everyone's roles than it is of practical value.

<div style="margin: 1em auto; text-align: center; max-width:900px;" class="mermaid">
---
title: Inverted Org Chart
config:
    theme: neutral
---
flowchart TB
    Joe & Mary & Jane --> M[Manager 1]
    Rob & Susan & Cory --> M2[Manager 2]
    M & M2 --> CEO
</div>

_Figure 3. The inverted org chart puts managers below their reports, and ICs on top._

To me, a more practical tool is the [North Star Framework](https://amplitude.com/books/north-star/about-north-star-framework), which aims to give autonomy to teams and individuals by taking top-level goals and breaking them down repeatedly. For example, you might start with a top-level goal such as increasing revenue by 15%. Then you break that goal into sub goals (eg increase customer retention by 15% and increase number of new customers by 10%), which you assign to teams, and then break those into sub-sub-goals which you assign to sub-teams, and so on.

### When to use it

I like thinking of leadership by autonomy as the default way an org should work, especially medium and large orgs. For the huge set of problems that can be broken down into sub-problems and tackled independently without too much coordination, this technique is very powerful. Not to mention empowering teams to solve problems on their own is very motivating.

### Pitfalls

Not all problems break down neatly into sub-problems -- many require coordination of multiple teams or even the whole company. That doesn't mean this style doesn't ever work, it just means you should reach for a different tool for problems that require coordinated effort or specific cross-team outcomes to achieve.

# Leadership by involvement

### What it is

Instead of giving autonomy, some leaders choose to focus on involving themselves deeply in day-to-day work of the team. Some people call this "[founder mode](https://paulgraham.com/foundermode.html)", although I'm not sure that term has a clearly agreed-upon definition.

### When to use it

When I think of a highly involved and highly effective leader, they remain experts in their products, they work with employees at every level of the org, and are invested in details. Leaders who deeply understand their product and the details of it can be highly effective when engaging employees throughout the org in many aspects of decision making.

As you involve yourself deeply, you should never give the impression of taking over. This style of leadership already reduces autonomy, and that only works if people have confidence in you and feel like your involvement is at least collaborative. This also allows you to operate with your team without understanding each and every tiny detail.

### Pitfalls

Of course there's a limit to how many decisions a single leader can be involved in, so you need to think carefully about how to scale this style of leadership. As you grow, you need to have clarity about which decisions you need need to be involved in, and which you don't, and you need to have a system for letting the org make other decisions without you.[^orgdesign]

Furthermore, if there's already someone in place who's well suited to make decisions on a particular topic, you should let them do that. Getting deeply involved when you don't need to be will feel like micromanaging. In a case like this, it's better to just make your expectations clear.

If you don't know the details well, this kind of leadership can be the worst -- you don't want to be that micromanaging boss who doesn't know what's going on. For this reason, using this style when you are new to a company or a project is generally a disaster.

# Leadership by policy

### What it is

Writing careful policies is an opportunity to shape decisions without having to be personally involved in each of those decisions. It can also be helpful in driving clarity for yourself -- the rules you lay out for others should be the same you use for yourself, after all.

### When to use it

Leading with policy works best for decisions that are repeated, such as hiring, promotions, making small technical or product decisions, and so on. As a company grows there are more and more of those kinds of decisions, so it becomes more and more helpful to have well-written policies.

### Pitfalls

Too much leadership by policy (especially when overly nuanced, detailed or confusing) can make a company feel inflexible and bureaucratic. When big companies try to cover too many cases with policy and complex approval processes, just navigating all the rules can start to soak up everyone's time. Good policy is clear and simple, and has flexibility to cover a most cases.

A good policy is also explicit about when to step out of the way. Escalations should be a natural part of the process when someone thinks their case deserves different consideration. Ideally, all policies make this explicit and leadership is sympathetic to the judgement of its team. A simple phrase like "unless decided otherwise by the appropriate committee or executive" along with clear steps for how to escalate can go a long way to keeping a policy simple and flexible.

# Leadership by conviction

### What it is

Sometimes a problem requires more than just a decision -- it requires top-down coordination and top-down strategy. This is where leadership by conviction comes in. Leading by conviction means making a decision (or set of decisions) and getting everyone to buy into it.

### When to use it

The only way this method works is if you are able to fully absorb all the info needed to make the decision yourself, otherwise you will make the decision incorrectly. If you can absorb the full context, make a good decision about it and convince others you are right, this can be a good way to lead.

Company or department roadmaps and strategy often fall into this category. For example, if you need various teams to achieve certain objectives by certain dates or in certain ways in order to get to your next round of financing, it probably helps to think it through centrally and disseminate the information. The critical thing here is providing clarity about the decision and making sure everyone understands the reasoning, and can get behind the decision easily.

### Pitfalls

The obvious downside of this style is how little autonomy it gives your team. However, if they are bought in, they will appreciate the clarity it provides. If they are not bought in (ie if the decision is wrong and they know it) it can lead to resentment and loss of trust.

If taking the time to get buy-in isn't possible, be ready for the repercussions of upsetting someone. I've heard stories of people walking out or even quitting on the spot when this goes wrong. I like to get buy-in by meeting with everyone one-on-one (in order from the most impacted to the least). I work hard to incorporate whatever feedback I get.

# Leadership by consensus

### What it is

Sometimes you need to make a coordinated decision and can't afford the political risks of leadership by conviction. Or perhaps no one person has all the context needed to make the right decision. In these cases, you need to drive consensus by bringing everyone together and agreeing on a course of action.

### When to use it

While it might seem like a slow process,[^slow] the kind of deep buy-in that comes from a true consensus can be extremely valuable: everyone feels like they contributed to the results and everyone feels motivated to follow through on the plan.

I like to use consensus whenever I can because I want everyone motivated and fully bought in. I also like to use it any time no one person understands all the details, because then you need to make the decision together anyway.

### Pitfalls

Sometimes leadership by conviction can masquerade as leadership by consensus. This means a leader pretends to get consensus, but they consistently reject feedback and disagreement and only consider the matter resolved when their point of view prevails. I've seen charismatic leaders get away with some of this kind of ugly behavior without too much bad blood, but I think they'd be better off admitting that they are the one making the decision, rather than pretending it's a group decision.

Leadership by consensus can run into trouble when leaders are listening, but people aren't willing to honestly speak up about their concerns. This is usually a sign of a deeper problem like lack of trust.

Consensus also needs to be used judiciously. If it's used too much for every problem you will never move forward. Your business needs ways to make lots of fast decisions and consensus is not one of them. But it is a great way to make important and complex decisions.


# Notes

[^orgdesign]: Dan Hockenmaier [writes](https://www.danhock.co/p/designing-an-org-for-founder-mode): "founder mode organizations maximize the number of decisions made by the founder, up to the limits of their ability to make better or faster decisions." I think it's important to figure out how you decide what to decide.
[^slow]: Will Larson [argues](https://lethain.com/developing-leadership-styles/) that, "Consensus has a reputation for being slow, but I think that’s an overstated concern. In situations where no one has the entire relevant context, there’s no particularly quick solution to making a robust decision."
