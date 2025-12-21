---
layout: single
title:  "Why I'm not adopting the 'AI-First' approach"
categories: management
excerpt: AI is a powerful too with tons of potential, but being "AI-First" is not the right way to make use of it.
header:
    overlay_image: "/assets/2025/first30-dark.jpg"
    og_image: "/assets/2025/first30.jpg"
    teaser: "/assets/2025/first30.jpg"
---

In the past few months, a few companies have announced they are going "AI-First". Not everyone is onboard with this: Duolingo, for example, came under a lot of fire for [their announcement](https://www.linkedin.com/posts/duolingo_below-is-an-all-hands-email-from-our-activity-7322560534824865792-l9vh/#). Most of the backlash they received came from people accusing them of replacing contractors and human nuance with AI.[^duo] That's a worthwhile conversation, but I'm here to consider something else: why the "AI-first" mindset is bad for business.

# Default Solution to Every Problem

What does it mean to be "AI-First"? One definition says that, ["The AI-first mindset involves prioritizing and using AI as your primary interaction for things like decision making, innovation, communication, creativity, and problem solving."](https://www.forbes.com/sites/ronschmelzer/2024/08/25/what-is-an-ai-first-mindset/)

I've seen a few other definitions, but the key element is the idea to change the culture of the company so that everyone considers using AI to solve every task before trying to solve the problem via other means. ie, ["Start with AI for every task"](https://www.linkedin.com/posts/nglance_engineering-ai-activity-7322657005800759297-QhRI), says DuoLingo's Chief Engineering Officer.

I've got a few problems with the idea of jumping to AI first for _everything_.[^luddite]

# AI shouldn't be thinking for you

The first reason for not using AI for everything is that the output is not always the important part of the job. When someone asks you to write a strategy, producing a nice, well argued text is not the important part. The important part is to think through the options and come up with a solution that is best for the company, and to deeply consider the answer using all the context you have. AI is not deeply considering anything for you, and isn't helping you understand why the strategy might make sense, it's just giving you an answer that looks nice. A result that makes it look like you did the assignment, when you actually did not.

In the case of writing in general, I'd go further and cite Paul Graham, who points out, ["writing is thinking"](https://paulgraham.com/writes.html). I agree and would also say that if you are outsourcing your writing to AI, you are outsourcing your thinking. For important work, we shouldn't let someone else do the thinking for us.

I'm not suggesting you should never use AI for correcting your grammar, or for tasks like summarizing or formatting. Rather, I'm saying that if you are using AI to do any core piece of writing for you, you are robbing yourself of the opportunity to think things through and truly understand the situation you are writing about.[^thinking]

Even for menial tasks like summarizing or formatting, I've seen problems. I've seen lots of examples of people at my company using AI to summarize a thread or write a ticket, but without the full context and without careful review, AI makes mistakes, which leads to more back and forth as I try to get clarity. It's become a bit of a pet peeve of mine when I when have to point something out that doesn't make sense (which is usually the point when the author confirms my suspicion that it was written by AI and they didn't review it).

I do sometimes have conversations with AI where I get additional ideas, or have it flesh out some bullet points. For example, I might ask it for advice on giving feedback to someone about a specific issue, but I always write the feedback myself.

# AI shouldn't be used to solve problems you can't solve yourself

A lot of folks are using AI for coding, but I haven't seen good success with AI taking over larger projects or projects that can't be solved by the developer themselves. AI works best at filling in boiler plate, and filling in details, but not overall structure.

The best coders right now are the ones who are planning out their work, breaking it down into pieces, and then asking the AI to fill in the pieces. When using AI for coding myself, the less I understand the problem and come in with a plan the more time I have to spend asking questions, rewriting code and otherwise cleaning up the mess.

Here, again, I do like to use AI to bounce ideas off: "How would I implement blah feature using blip constraints? Is the best thing to foo, or are there better approaches?" Conversations like that often leads me to understand the problem better. If it says something I don't understand I can dig in and AI becomes like a personal tutor, which is currently my favorite way to use AI, even if it can sometimes be wrong.

Maybe someday, AI will be better at solving problems you can't solve yourself, but for now, if you _can_ solve the problem yourself, it _is_ good at taking away some of the menial bits of the job.

# AI is mediocre

The theme in the above examples is something that many have observed: AI is great at doing mediocre work. If you have lots of semi-repetitive work to do that requires minimal thinking, by all means please use AI.[^mediocre]

But if you need someone to do an excellent job especially on a task that requires deep context (such as writing your company strategy), don't outsource the job to AI. And definitely don't outsource the task to AI if the process of producing the work is as important as the end result itself.

A recent study[^mit] by MIT agreed: "AI has already won the war for simple work, 70% prefer AI for drafting
emails, 65% for basic analysis. But for anything complex or long-term, humans dominate by 9-to-1 margins."

# What I am doing instead

So how am I using AI, and how am I adopting it as an engineering leader? I love AI as a tutor, asking it to help me think through a problem and by asking it questions around things I don't understand. Sometimes I try to have a conversation with it to poke it's brain. It's a bit harder to poke AI's brain than to poke a person's brain because of how reluctant it is to disagree with you, but I've found it can be very helpful when prodded the right way.

As for encouraging its use at the company level, the fist thing I prioritize is making sure everyone is familiar with the tools. I don't track AI output, and I don't treat all AI usage as good.[^leaderboard] But I do encourage experimentation -- making sure everyone has the tools, having explicit learning sessions for people to show us their workflows, etc. My specific goal for H2 or last year was decidedly modest: ensure that 75% of engineers are using AI tools on any given week, and that they are trying it out for a variety of use-cases. Beyond that, I trust my team to use AI where it makes sense -- and not for every task.

For products, AI works best in an existing workflow, where it can replace humans in mundane tasks, rather than entire workflows where more context is required. For example, in our [Card adoption workflow](https://www.rutter.com/supplier-enablement), we created a complete workflow to help payment card issuers get their customers to switch to their card. Rather than attempting to have AI manage this entire workflow, we used a traditional codepath that initially used humans to fill in the missing gaps. We are able to slowly replace the humans in the loop with AI because we gave it narrow tasks for which the amount of context is limited, there are easy mechanisms for feedback and learning, and exceptional thinking is not required.

# Bottom line

AI works best when you can understand and break the problem down yourself, then assign the parts that require mediocre thinking to AI. If, instead, you are using AI first for everything, you are going to spend a lot of time getting AI to give you mediocre results.

# Notes

[^luddite]: To be clear, I'm neither a luddite nor an AI nay-sayer, but I have seen a number of new technologies find their way into far more places than they belong because of hype. While I agree with the claim that "AI is different" from previous technology changes, it's not so different that it should become the default for every problem.
[^duo]: [The backlash didn't seem to matter much for their business](https://techcrunch.com/2025/08/07/the-backlash-against-duolingo-going-ai-first-didnt-even-matter/)
[^thinking]: In fact, I feel so strongly about this that I don't use AI for this blog at all. The point of this blog is for me to think through important topics for myself, and I can't do that if AI is doing the thinking. I do like the cute red panda character it generates, but if art were the core point of this blog I would probably be forced to admit how mediocre that is, too.
[^mediocre]: I like the way the Economist put it: AI excels at tasks that, "[don’t need a deep understanding of the company, and are 'easily verifiable'](https://www.economist.com/business/2025/12/01/lessons-from-the-frontiers-of-ai-adoption)."
[^mit]: Yes, this is [THAT](https://mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf) MIT Study.
[^leaderboard]: I've heard of some companies creating leaderboards of people who use AI the most, and reward people for using AI, as if all AI usage is good. This reminds me of companies that used to track how many lines of code their employees wrote.