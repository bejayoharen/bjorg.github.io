---
layout: single
title:  "Engineering team growth part 2: The interview panel"
date:   2024-12-12 01:01:00 -0400
categories: management
excerpt: Most interview panels include people with varying degrees of skill and experience. It’s important to prepare them for the task.
header:
    overlay_image: "/assets/images/team-growth-1-dark.png"
    og_image: "/assets/images/team-growth-1.png"
    teaser: "/assets/images/team-growth-1.png"
---

*This is part two in a [series on Engineering team growth](/series/engineering-team-growth/). I suggest you read [part 1](/management/engineering-team-growth-1-job-description/) first, where I explain how to write a good job description. Having a good job description is critical because it’s the document that everyone on the interview panel should understand and be bought into. There should be no doubts about what is and isn’t required for the job. The next step is to choose people for the interview panel, and break down the requirements into concrete interview plans.*

# Selecting your interview panel

When picking people to be on your interview panel, there’s more to consider than just who can do the interview for which skills (although obviously you’ll need to make sure that’s covered!). For example, you want to make sure the team you are hiring onto is well represented, so that they are bought into the decision when it comes time to make an offer. You want them to be excited to welcome a new team member, not resentful of a change they had no voice in making.

I like to include as many people from the team as possible. I’ll even have people pair-interview just to include more people.[^pairing] Having more people can make scheduling and decision making more complex, so it’s a trade-off, but I prefer to err on the side of including more people when I have that luxury.

Depending on the role, you might want to include important stakeholders. For example, for an SRE role, you might want to include some of your most senior engineers from other teams, and for an integration engineering role, you might want to include someone from business development.

I’ve worked at companies that have separate “culture fit” or “another perspective from another department” type interviews, but I recommend against them. These are a waste of time at best and biased at worst. Instead, I prefer to evaluate soft-skills like communication, collaboration, empathy and prioritization explicitly.

Many companies always include someone like the CEO or other leader. These leaders often don’t have objective criteria they use in the interview. Sometimes they go in completely unprepared, and their decision usually comes down to who they like. However, a good leader won’t override the hiring manager’s decision unless their objection is reasonable. Their involvement has other advantages: it signals to the candidate the importance of the role, while giving them a chance to ask the higher-up questions about the rest of the company. It’s also a good sign when someone like the CEO understands the importance of hiring, even if they aren’t fully embedded in the process.

# Establishing test criteria

In engineering, we often default to a particular set of interviews, eg one coding interview, one systems interview, and one product interview. This often works well, but don’t fall into the trap of assuming that’s the right setup for every hire. Instead, tailor your questions for the role by focusing on the requirements in the JD. If you find you need to test for things not on the JD, you should revise the JD so everyone, including candidates, are clear on the expectations.

Let’s look at a simplified JD and figure out how to break it down. A common challenge is finding someone who is an expert in one domain, but still needs to be competent in other domains. This example would be for a Front End engineer who might need to do some work on the backend, eg if they need a tweak to an endpoint to add a new feature.

> Example (simplified) JD requirements section:
> 1. Debug subtle issues, build complex new features, and keep code up to date with the latest standards in a complex Javascript, Typescript and React codebase.
> 2. Support and mentor less experienced teammates in solving technical problems.
> 3. Navigate a complex Python/Django codebase and make simple changes, including bug fixes and features.
> 4. Communicate with stakeholders, including developing estimates, informing of delays, and collaborating to find creative solutions.
> 5. Skilled at understanding user intent, and working with the design team to provide intuitive solutions to users' problems.
> 6. Able to prioritize projects with little guidance.

You’ll want to assign testing for the first criteria to a panelist who’s very experienced in Javascript, Typescript and React. That panelist will need to come up with a good way to test as objectively as possible. Rather than writing fresh code, evaluating a candidate’s skill might include showing them some out of date code, asking them to identify issues, and ask how they would address the issue. This kind of test asks the candidate to do something that's more representative of the kind of work they might do on the job.

The same panelist, in the same interview, can also test for the second criteria by asking follow-up questions like “how would you explain that decision to another developer who doesn’t have experience with hooks?”

How well candidates perform on each of those questions would be the basis for a clear rubric. The interviewer should go in prepared with the question, and an idea of what good and bad answers look like. For example:

> * The candidate was able to identify the incorrect use of global variables.
> * The candidate was able to suggest a better solution.
> * The candidate was able to explain the solution in terms a less experienced engineer would understand.

You can assign a number of points to each item if you want to score like a teacher would score a test, or you can just check each item they did.

# A word about leetcoding

At the risk of jumping into the debate about white-board and leetcoding interviews, I'll state my opinion on them. In general, with the rise of remote interviews and AI assistants that can be used to ace these questions, I think leetcoding is growing less useful. Having both aced and failed in-person white-board leetcoding interviews myself, I have to wonder how useful they ever were.

However, I'm not completely opposed to them either. They aren't the best representation of work we do as software engineers, but it's hard to be really good at software engineering without being able to write some challenging code, so I still keep them handy in my toolkit for times when I don't have a clearly written JD, or we are hiring a junior engineer, who might not yet be great at real-world tasks. I particularly like simple white-boarding questions for junior and intern engineers, who still need to learn on-the-job skills and what you really need to assess is if they can write code.

Regardless, I recommend avoiding anything too common (like "reverse a string" which practically everyone has done already) or too tricky (like "find all prime numbers from 1 to 1000" which requires knowledge of the sieve of Eratosthenes or else it becomes overly complex). Simple tasks that require two preexisting data structures work well (e.g., "find the most common word in a given list"). I don't believe these tests can be used to determine someone's overall experience or the depth of their knowledge or experience, so I don't see too much point in making them overly complex or tricky.

# Post Interview

I’ll say more about how to actually conduct interviews in my next post, but for now, let’s assume everyone has done their interviews and evaluated the candidate based on their rubrics. What’s next?

Ideally, everyone should jot down their notes and the results of their interviews before talking to others. This helps ensure that everyone's opinion is heard and their initial impressions are documented. One panelist with strong feelings or persuasion skills can sometimes drown out important points made by others, or bias others into changing their mind before they've even given their opinion.

Trying to stop people from gossiping, however, is almost impossible, so I try to make jotting down the results as quick and easy as possible. I usually use a google form asking the interviewer the following questions:

* Did the candidate pass your tests? (1-5 + open-ended section to elaborate)
* Does the candidate have the right experience for the job? (1-5 + open-ended section to elaborate)
* How would you rate the candidate’s communication skills? (1-5 + open-ended section to elaborate)
 * How would you rate the candidate’s empathy? (1-5 + open-ended section to elaborate)
* Were there any red flags about the candidate? (eg did they speak overly negatively about a previous coworker? Did they have a cold or negative attitude about the task?)
* Overall assessment? (pass/fail)

# Extending an offer

As the hiring manager, you might have to override some objections. For example, I once had a panelist object to hiring someone because she felt the person wasn't going to be "fun" enough, even though that person passed all the tests. Since being "fun" wasn't part of the job requirements (I wasn't hiring an entertainer) I overruled that objection.

More challenging can be overruling an objection from a C-level panelist. I once had a C-level interviewer object that an engineer we were hiring didn't use social media. This was not a job requirement so it was easy to dismiss the objection, but it's important to be extra polite in these situations.

On the other hand, I knew a hiring manager who hired someone even after initially giving the candidate a poor evaluation. The rest of the panel was strongly in favor of hiring. He later told me that hiring that candidate was one of the best decisions he ever made and it taught him to "trust the process". In this case, his own objection wasn't a dealbreaker -- if a hiring manager truly feels the candidate isn't up to the job, they can and should make the call not to extend an offer. If it's not clear if something is a dealbreaker, I like to compare the objection to the job description and use that as a reference. If it's still unclear, my recommendation would be to reject the candidate and consider revising the JD.

The final decision to extend an offer is usually up to the hiring manager, though it depends on the company (some companies allow anyone on the panel to reject a candidate, for example). My rule of thumb is: if the candidate passes the tests and there are no red flags (or you’ve investigated the red flags sufficiently) you should extend that person an offer. It would be nice to have multiple people to compare and pick the best one, but in engineering we don't usually have that luxury, which makes it all the more important we have clear criteria up-front.

Regardless, if someone on the panel disagrees with your decision to make an offer, be prepared. It may be worth having a one on one with the person who objected to let them know you hear their objections, but you are not taking their advice, and explain why. You don't want one of the panelists to be resentful about a hiring choice, so it's worth making sure they understand the decision, and feel like you heard them out.

# Acknowledgements

Thanks to [Chris Pepper](https://extrapepperoni.com) for his feedback on this post.

# Footnotes

[^pairing]: pairing on interviews has other benefits like keeping team members accountable for preparation, and training people who are less experienced at hiring.
