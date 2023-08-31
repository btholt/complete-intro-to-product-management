---
description: >-
  Learn about effective planning strategies in the tech industry, including the
  importance of having a plan, aligning with organizational culture, starting
  the planning process, sourcing ideas from various stakeholders, following
  themes, and structuring projects for completion. Find tips on milestone
  setting, prioritization, and communicating future needs through the cutline.
  Avoid common pitfalls by ensuring research and feasibility before adding
  projects to the roadmap.
keywords:
  - tech company planning
  - quarterly planning
  - effective planning strategies
  - aligning with organizational culture
  - prioritization
  - milestone setting
  - communicating future needs
---

Planning, everyone's favorite thing to do at tech companies. We get it wrong so frequently that it becomes a bit of a meme.

![xckd talking about how to correctly estimate engineering tasks](/images/xkcd.png)
<sup>By Randall Munroe on <a href="https://xkcd.com/1658/">xkcd</a></sup>

If you are hoping that you are going to roll into this section and reveal the golden secret of how to plan well, well, I have bad news for you. I am just as bad at it as everyone. Perhaps my only leg up is that I know I am just as bad as everyone else is, and I just plan around the fact that plans are definitely going to change. And I do have some high-level advice for when it comes to planning, so let's get to it.

First, what kind of planning are we talking about? Generally, I am speaking of near-term planning. For every tech company I have worked for so far, that has taken shape as quarterly planning. The way each of these companies has gone about doing this has varied quite a bit, but the time frame has been consistent: planning for three months at a time, [usually centered around the fiscal quarters][quarter]. Because of that, I am going to address you as if you are also doing some sort of quarterly planning, but this principle would apply to doing half-year or full-year planning as well.

## Plan

The first tidbit is you should plan. If you are at a startup and you are not doing some sort of planning, you should start, even if it is not for rigid quarters. Just having some sort of loose, prioritized roadmap that says, "After we finish this task, we plan to do this task," will keep your team on-task and executing the most important things. Without some sort of plan, you tend to suffer strongly from [recency bias][bias], where you tend to work on the things that you have been most recently thinking about, which is not always the most effective thing. It is a useful task every so often to sit down with your team and say, "Did we do the right things? Are we doing the right things? Are we about to do the right things? What should we do later? What should we not do?"

## Fit into your org

Assuming your company has some sort of culture around planning, my advice for you is to find a way to plug into it. You can definitely bring your own spin and experience to it, but the whole point of planning is to drive alignment across an organization. If you are off doing something that doesn't fit, you are neither aligning with your sister teams nor are they going to view you as a reliable team to partner with. For me, this has meant wildly changing my planning style each time I changed jobs. At Stripe, I essentially just made team strategies while the eng managers made the plans, and now I make nearly the whole plan myself.

## Start

This is sort of universal advice for being a product manager, but this helps me a lot, particularly with planning. It can be a daunting prospect to start a planning process. The best way to finish is to start. That sounds like a truism (and it is lol), but more concretely, what I mean is just open a doc and start writing. Start with literally anything that is in your brain and start putting it on "paper." You don't have to start from what will be the beginning of the doc, and you don't have to keep anything that you write. Just start writing. Once you're writing, I promise the wheels will start turning, and you will start getting to what you actually want.

## It shouldn't be all your own ideas

It may feel like the PM has to come up with all the ideas that the team works on. Not true at all! I would venture to say most ideas _shouldn't_ come from you. They should be sourced from your users, your team, your company, and anywhere else that could be a good source of good ideas. I would venture to say that recently, 50% of my roadmaps are ongoing tasks, 40% came from either my team or my great company, and 10% came from me. It's not always like that; it'll ebb and flow depending on what is important.

Pro tip here: When you are about to head into planning, about a week before, hold a brainstorming session with your team. I have gotten so much out of it that it feels like cheating. On top of the awesome ideas your team comes up with, they feel heard and represented on your roadmap, which is critical. When an engineer gets to work on their idea from start to end, they feel empowered, which is just awesome.

## Follow the themes

Some companies explicitly publish themes for their PMs to plan around: reliability, cost reduction, UX improvement, growth, etc. If yours does, make sure to align. If not, chat with your other product leaders to see what they are working on. Sometimes, you will see some themes arise just ad-hoc, in which case aligning your team with others can provide some boons. Is everyone looking to reduce costs? It might be useful to have your engineers take advantage of the momentum and collective thinking. It also might not, just a suggestion to look for. If you have themes in your work, list them on your roadmap.

## Make projects completable

Be sure to phrase the projects on your roadmap as something that finishes. Don't say "improve web performance," as that isn't completable. That project never ends. You never get to check it off, as web performance is an evergreen problem. Instead, be specific, like "swap out slow framework for fast framework" or "migrate API to new faster infrastructure" or something you eventually get to check off. If you can't even be that specific (really do try), then timebox it. "Two-week perf push" or something like so at least it ends.

## Make long projects have milestones

Frequently, you will end up with a really long project that may take longer than the quarter. In these cases, define milestones that do get completed within the quarter. If you have a year-long migration from Oracle Cloud to Microsoft Azure, make the first quarter's goal "Milestone 1: Migrate databases" or something like that so your goals are still completable within the quarter. This helps keep you and your sister teams correctly accountable and helps you communicate where you expect to be after the quarter.

## The Cutline

Differing companies will have different ideas of how much you should plan for. Google famously says that if you completed more than 80% of your roadmap, then you didn't plan enough things to do. Other companies expect that if it makes it on your roadmap, then you are committing to finish it. Whatever they choose to do, follow those.

However, let me show you a powerful way to drive alignment and sometimes even get extra funding. The magical cutline. However you choose to communicate it, you want to somehow say, "Here's what I would work on if I had more people." This shows other teams what you are thinking about and choosing other things above it. It also communicates to management, "If you give me more people, I will do these things." It also can happen where leaders will come in and say, "We think this is more important, so please prioritize it," which I appreciate because then it helps us have important conversations before they become problems.

## By the time it's on the roadmap, it should be researched

I have made this mistake more than once. By the time planning rolls around, I have been working hard to finish the end of the quarter strong, and I won't have been thinking enough about the next quarter. Then, when planning is happening, I will put some projects as wishful thinking, "Hey, we have the capacity, and this is a cool idea; let's put it on the roadmap!" only to find out what I listed is either much harder than I thought, actually impossible, or relies a lot on sister teams that don't have the capacity to support me.

This is all to say by the time you get to planning, make sure you have ironed out the basic details. It is even better if you can have a product spec or at least the start of one. Make sure you are working within the realm of possibility and that any inter-dependencies have been communicated and can be relied upon.

[quarter]: https://en.wikipedia.org/wiki/Fiscal_year
[bias]: https://en.wikipedia.org/wiki/Recency_bias
