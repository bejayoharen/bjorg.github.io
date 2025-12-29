---
layout: single
title:  "Why I won't be 'AI-First' in 2026"
categories: management
excerpt: AI is already a powerful tool, with tons of potential on the way. Being "AI-First" is not the right way to make use of it.
header:
    overlay_image: "/assets/2025/first30-dark.jpg"
    og_image: "/assets/2025/first30.jpg"
    teaser: "/assets/2025/first30.jpg"
---

In 2025, a lot of companies announced they are going "AI-First". Not everyone likes this: Duolingo, for example, came under a lot of fire for [their announcement](https://www.linkedin.com/posts/duolingo_below-is-an-all-hands-email-from-our-activity-7322560534824865792-l9vh/#). Most of the backlash they received came from people accusing them of replacing contractors and human nuance with AI.[^duo] That's a worthwhile conversation, but I'm here to consider something else: why the "AI-first" mindset is bad for business.

What does it mean to be "AI-First"? The key element in being AI-First is a company culture in which everyone considers using AI to solve every task before trying to solve the problem via other means.[^def]

I've got a few problems with the idea of jumping first to AI _everything_.[^luddite]

# AI lacks context

The first reason for not using AI for everything is that the output is not always the important part of the job. When someone asks you to write a strategy, for example, producing a nice, well argued text is the part AI can do well, but it's not the important part. The important part is thinking through the options, given all your context, and coming up with a solution that is best for the company. It is necessary to deeply consider the answer using all the information you have about the state of the market and teh company -- information with the AI doesn't have and is relatively hard to give it.

In a job like this, AI is not deeply considering the information you have, and isn't helping you understand why one strategy might make more sense than another. AI is just giving you an answer that looks nice. The result is a document that makes it look like you did the assignment, when you actually did not.

# AI shouldn't be thinking for you

In the case of writing in general, Paul Graham argues that ["writing is thinking"](https://paulgraham.com/writes.html). If you are outsourcing your writing to AI, you are outsourcing your thinking, and for important work, we shouldn't let someone else do the thinking for us.

I'm not suggesting you should never use AI for correcting your grammar, or for tasks like summarizing or formatting. Rather, I'm saying that if you are using AI to do any core piece of writing for you, you are robbing yourself of the opportunity to think things through and truly understand the situation you are writing about.[^thinking]

Even for menial tasks like summarizing or formatting, I've seen problems. I've seen lots of examples of people using AI to summarize a thread or write a ticket, but without the full context and without manual review, AI makes mistakes.

# AI shouldn't be used to solve problems you can't solve yourself

The best coders right now are the ones who are planning out their work, breaking it down, and then asking the AI to fill in the pieces. The less I understand a problem the more time I have to spend asking questions, rewriting code and otherwise cleaning up the mess that AI coding tools tend to make.

I haven't seen good success with AI taking over larger projects or doing any sort of work that can't be solved by the developer themselves. AI works best at filling in boiler plate and filling in details, but planning organizing is still a challenge.

Maybe someday, AI will be better at solving problems you can't solve yourself, but for now, if you _can_ solve the problem yourself, it _is_ good at taking away some of the menial bits of the job.

# AI is mediocre

The theme in the above examples is simple: AI is great at doing mediocre work, but not much else. If you have lots of semi-repetitive work to do that requires minimal thinking and minimal context, by all means please use AI.[^mediocre]

But if you need someone to do an excellent job especially on a task that requires deep context (such as writing your company strategy), don't outsource the job to AI. And definitely don't outsource the task to AI if the process of producing the work is as important as the end result itself.

A recent study[^mit] by MIT agreed: "AI has already won the war for simple work, 70% prefer AI for drafting
emails, 65% for basic analysis. But for anything complex or long-term, humans dominate by 9-to-1 margins."

# What I am doing instead

So how am I using AI, and how am I adopting it as an engineering leader? I love AI as a tutor, asking it to help me think through a problem and by asking it questions around things I don't understand. It's a bit harder to poke AI's brain than to poke a person's brain because of how reluctant it is to disagree with you, but I've found it can be very helpful when prodded the right way.

As for encouraging its use at the company level, the fist thing I prioritize is making sure everyone is familiar with the tools. I don't track AI output, and I don't treat all AI usage as good.[^leaderboard] But I do encourage experimentation -- making sure everyone has the tools, having explicit learning sessions for people to show us their workflows, etc. My specific goal for H2 or last year was decidedly modest: ensure that 75% of engineers are using AI tools on any given week, and that they are trying it out for a variety of use-cases. Beyond that, I trust my team to use AI where it makes sense -- and not for every task.

For products, AI works best in an existing workflow, where it can replace humans in mundane tasks, rather than entire workflows where more context, and more complex thinking is required.

# Bottom line

AI works best when you can understand and break the problem down yourself, then assign the parts that require mediocre thinking to AI. If, instead, you are using AI first for everything, you are going to spend a lot of time getting AI to give you mediocre results.

# Notes

[^duo]: [The backlash didn't seem to impact the business](https://techcrunch.com/2025/08/07/the-backlash-against-duolingo-going-ai-first-didnt-even-matter/)
[^def]: Here are [two](https://www.forbes.com/sites/ronschmelzer/2024/08/25/what-is-an-ai-first-mindset/) [definitions](https://www.linkedin.com/posts/nglance_engineering-ai-activity-7322657005800759297-QhRI) from advocates of the idea.
[^luddite]: To be clear, I'm neither a luddite nor an AI nay-sayer, but I have seen a number of new technologies find their way into far more places than they belong because of hype. While I agree with the claim that "AI is different" from previous technology changes, it's not so different that it should become the default for every problem.
[^thinking]: In fact, I feel so strongly about this that I don't use AI for this blog at all. The point of this blog is for me to think through important topics for myself, and I can't do that if AI is doing the thinking. I do like the cute red panda character it generates, but if art were the core point of this blog I would probably be forced to admit how mediocre that is, too.
[^mediocre]: I like the way the Economist put it: AI excels at tasks that, "[don’t need a deep understanding of the company, and are 'easily verifiable'](https://www.economist.com/business/2025/12/01/lessons-from-the-frontiers-of-ai-adoption)."
[^mit]: Yes, this is [THAT](https://mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf) MIT Study.
[^leaderboard]: I've heard of some companies creating leaderboards of people who use AI the most, and reward people for using AI, as if all AI usage is good. This reminds me of companies that used to track how many lines of code their employees wrote.