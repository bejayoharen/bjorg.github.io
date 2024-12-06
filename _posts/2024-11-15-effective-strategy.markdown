---
layout: single
title:  "Effective Strategy"
date:   2024-11-15 12:01:00 -0400
categories: management
excerpt: Strategy is an important and oft-misunderstood concept. Let's explore how a clear understanding can help you keep your team on track.
---

A coworker of mine once complained about the fuzzy meaning of the word “strategy” at our company. He would say, “it means something different to everyone. It’s like a Rorschach test.” He was not alone. Strategy expert Richard Rumelt argues that bad strategy is the norm. Bad strategy, he argues, involves “not just… the wrong goals or the wrong implementation” but rather “mistaken views about what strategy is and how it works”. Let’s talk about what makes strategy an effective tool.

# Definition of strategy

When most people think of strategy, they think of a high-level and medium to long-term plan. You might go further and think of it as a plan for changing a system from its current state to a desired state, or how to respond to changes in the market or other challenges.

That's a start, but effective strategy needs more than that. It also needs:

* An accurate diagnosis of the problem or opportunity
* A plan to focus the company’s effort[^focus-v-guiding]
* Concrete (and actionable) steps to achieve the desired outcome

Let’s break these down.

# Accurate Diagnosis

To make the right change in an organization, you need to accurately and honestly understand what the problem or opportunity is, as well as what advantages you have versus competitors. It’s no help planning a change when your understanding of the problem is wrong.

For example, in the early years of GIPHY, the CEO had one major initiative for each year. One highly successful initiative was stickers, which, once developed and integrated by major partners, doubled our traffic.

The reason we pursued this was because our CEO saw an increase in content, such as instagram stories, where people were “decorating”. That is, users would start with a photo or video, and add text, emojis, polls, and so on. We already had integrations with some of the major players in this space, and we already had some sticker content, so we were uniquely positioned to deliver content to decorate with.

Mistakes I’ve seen at the diagnosis stage include believing an opportunity exists when it doesn’t, believing you have an advantage you don’t really have, or underestimating competitors. In engineering, we often overestimate the value of major initiatives like migrations or bringing on new technology. It’s also easy to underestimate the value of solving processes and team problems.

# Focus

A good strategy focuses the company. In its natural state, a company will try to tackle every opportunity that might give it an advantage. At smaller companies, it’s sometimes hard to get the data to know where to focus, and at larger companies ambitious managers seek out opportunities to prove themselves with their own pet projects, regardless of how in-line those projects are with the company focus. Even if all of these side-projects are a win, working on disparate goals dilutes the effort that could be spent on the single most lucrative goal.

In GIPHY’s stickers initiative, leadership made sure everyone focused their efforts on stickers, and not on other less impactful things. This ensured we got it done from start to finish with maximum impact.

This was a major effort, but it was tractable: Outside engineering new content had to be sourced and partners had to be convinced, and inside engineering we needed to complete some stickers-related features we had already started and build some features to demonstrate the value of stickers to partners. Since stickers were just GIFs with some transparent pixels, and our API endpoints already allowed users to search for stickers as their own content type it wasn’t immediately obvious that product and engineering had to do much to support the focus on stickers.

However, product and engineering were still critical to the initiative for two reasons: 1. We needed to make sure that work we did need to do was completed quickly so we would not slow down other teams, and 2. There were product features that could be developed to demonstrate the value of stickers to partners. Having a company-wide focus on stickers meant that every team understood the priority and that other projects, even important ones, would take second stage to stickers.

Creating focus, however, is one of the biggest challenges because focusing effort involves saying no to many people and projects, including ones that would add value, but I would go so far as to say if you aren’t making tradeoffs, and saying no to competing initiatives, you probably aren’t making a strategy.

# Concrete steps

Beyond focusing the company on a specific goal or small number of goals, Leadership also needs to define concrete steps to achieve the goal. This often takes the form of smaller goals that ladder up to, or lead to the main goal. Without these steps, focus is hard to achieve, and people may not understand how the goals are going to be achieved.

For example, when GIPHY was building stickers, the key steps were:
* Create demonstration products to help sell the concept of stickers to partners.
* Add enough sticker content to make sure all popular search terms were served.
* Sell the sticker API integration to partners we already had relationships with.

As far as creating demonstration products, one team built a VR app that used stickers and managed to win some high profile awards. My team rebuilt our GIF upload tool to allow users to decorate existing GIFs with stickers. Although popular and fun, these were not features that would have been worthwhile to build on their own – they were worthwhile as part of a focused company initiative to get partners using our sticker integration.

Even in the face of some failures along the way, GIPHY was able to win the stickers market because it accurately identified an opportunity, focused the company’s effort on stickers, provided guidance for what mattered and what didn’t, and had a concrete plan to get there from where we were.

# Antipatterns

There are lots of ways a strategy can go wrong, but one I want to focus on is the laundry list of goals. I’ve seen vibrant companies completely stall with this approach. Leaders may be afraid to push back on the goals of competing factions, or they may believe in some sort of magical thinking that by giving people a list of lofty goals and inspiring them with an ambitious message is what leadership is about. While there’s no doubt that being an inspiring leader can help, the idea that inspiration can take the place of real strategy work has, unfortunately, taken over many corporate boardrooms.

One CEO of a publicly traded company I worked at subscribed to the laundry list of goals philosophy. Had he been a more inspiring leader, this might have worked to some extent, but when push comes to shove, you can’t win by spreading your company out. A good leader communicates what the priorities are and coordinates effort across a company towards those priorities, rather than diluting the effort with a dozen goals. That’s hard work, but it works.

# Resources

In the future I plan to write a bit more about Engineering Strategy specifically, but, in the meantime, Will Larson has [some great writing on the topic](https://lethain.com/strategy-notes/).

The best resource I know of on strategy in general is [“Good Strategy/Bad Strategy”](https://www.amazon.com/Good-Strategy-Bad-Difference-Matters/dp/0307886239) by Richard Rumelt, which I highly recommend.

# Footnotes

[^focus-v-guiding]: Instead of focus, Richard Rumelt, suggests a good strategy has a guiding policy. I agree that the focus should be driven by a coherent policy, which helps teams make decisions. I decided to write about focus instead of guiding policy, because, in my own experience with good and bad strategy, I’ve seen focus be the main deciding factor of success. The guiding policy is important because it helps other leaders in the organization make decisions that support the strategy. The guidance might come in the form of specific initiatives that need to be prioritized, a guiding principle, or a timeline of intermediate objectives that need to be accomplished. Regardless, I think Rumelt would agree that the purpose of guidance is to create focus.