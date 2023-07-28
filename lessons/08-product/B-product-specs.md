---
description: >-
  Learn how to write an effective product specification (spec) that proposes a
  project and aligns everyone involved. This guide covers the important sections
  of a spec, including the executive summary, problem statement, goals, key
  metrics, rollback criteria, timelines, designs, technical concerns, and
  appendix.
keywords:
  - product specification
  - product spec
  - project proposal
  - executive summary
  - problem statement
  - goals
  - key metrics
  - rollback criteria
  - timelines
  - designs
  - technical concerns
---
This document goes by many names: the product specification, proposal, sheet, etc. but we're going to call it a "spec" here. It is what you as a PM write to propose a project and get everyone aligned and moving in the right direction. I would argue that these are the most important docs you right (up there with the team charter docs.)

> I am going to give you some of my tips and tricks of making my product specs work but know this is also an inexact science. You can do things totally different still be successful. So take this as input into your system rather than treating this as law. I've seen a myriad of varieties of how people write these and each of their own boons and downfalls. This is just my current thinking as of right now of how I write my product specs.

A product spec describes a parcel of work of some variety, usually around some enhancement to an existing product or a new product all together. It takes care to describe in depth what it should do, how it will accomplish it, how success will be measured, and any context necessary to make the changes being described.

## Most important to least important

Assume people will start reading at the top and drop off the more you write. Generally this is true as we have seen before so lean into it; put the most important stuff first and the least important stuff. This will somewhat vary project to project but in general the way I organize mine is:

1. The BLUF / Executive Summary
2. The Problem Statement / User Stories
3. Goals and Non-Goals
4. Key Metrics
5. Rollback Criteria
6. Timelines
7. Designs / Mocks
8. Technical Concerns / Outstanding Questions
9. Appendix 

Some projects will have less than this, and some will have more. This is a loose framework to play with and adapt, not any sort of rules. You can reorder them as needed for you. You can add and subtract sections as necessary. Make it yours.

My overarching principle here remains the same: order it so that more people will read the sections you want them to read it. Get from people what you need from them.

Let's dig into the sections

### The BLUF / Executive Summary

I write this last. I will usually let an AI client (for me usually Notion's AI since that's approved for me to use at work) start a summary of the doc and then edit it so it really drives home whatever point I am trying to make. In any case, this is meant to be 2-4 sentences that summarizes what problem exists and what we are going to build to make it better than it is. For some it is enough for them to stop reading and move on and for others it gives a general framework for what they are about to read. Keep it short and ruthlessly to the point. No fluff here.

### The Problem Statement / User Stories

Here I will go and describe more in-depth what the actual problem is that we are trying to solve, how we discovered it was a problem (our metrics said so, our users are tweeting it, the support tickets, or we are just making a bet that this is a good idea), and then the proposed solution. Frequently I will literally list the user stories we are tackling so that people can see the user-rooted ideas we are chasing. The key here is that someone walks away with an understanding that there is a problem, why we know it is a problem, and our intentions to solve it.

> **Minimum Lovable Product**: I imagine many of you have heard the term "minimum viable product" as a way of describing how to build products. This is the idea that you should cut scope (scope being the breadth of work you are committing to) until you are the absolute minimum of what you can launch and it still work. I adhered to this idea for most of my career and honestly it works well for the most part. It gets you to ship products faster which in turn you can start learning from your users. I have shifted my thinking a little bit to chase the minimum lovable product. Some minimum viable products can cut out the parts that make them special in the chase of shipping faster and I think this can be frequently be a mistake. I try to preserve where possible what makes a product special and ruthlessly cut anything optional, tangential, or that doesn't impact enough of the targeted users. Try to find your balance.

### Goals and Non-Goals

This section is usually a short bulleted list of our explicit goals for the project. Things like reduce churn, increase sign ups, make more money, have less support tickets, etc. It doesn't need to be super elaborate but it helps a reader frame what things you are looking to do at a glance. The reader could probably intuit what these will be from the previous section.

The more important part here is the non-goals. Here is where you outline explicitly what you are _not_ going to do. This can be critical to a good product spec so that a reader can know "we are aware of this possibility and we are not going to chase it." It will reduce a lot of unnecessary conversations of obvious things around "did you think about this" when you already have and have chosen not to pursue it. It is also just a useful exercise in focusing in on your target and reducing scope creep.

> **Scope creep** is what happens when projects accidentally become larger, longer, more difficult, etc. because a team (usually the PM) is not vigilant in keeping a project and a team focused on achievable goals. It's when after a project is started the planning process that things keep getting added. Heavily guard against it or it will sink your product.

### Key Metrics

Now that someone reading your spec understands the scope of the project you can start talking about success and failure looks like. Key metrics are things you expect to track closely to see how the project is going. These will be a good gauge if the thing is actually working at all and how people are utilizing it.

A few thoughts here.

- Monthly active users (MAU) is a good metric that lots of people track. But it is not always the end-all-be-all of metrics. Take Microsoft Excel for a second. Imagine a user that uses Excel once a quarter to do quarterly reports and doesn't have need to use it outside of that. Is that user active? I'd say that is a successfully active user and MAU wouldn't capture that. It's good to look at several slices of that.
- If CSAT is the metric you're looking to affect, plan for a long tail. It takes a long time for CSAT to reflect new sentiments and it's hard to disentangle it from other things. Twitter could have made a lot of people happy with allowing longer videos or doing revenue sharing but tanked the CSAT by rebranding to X. Always pair CSAT with something more easily trackable.
- Your project metrics should almost always include one of your team's metrics, or at very least company core metrics. If not, why? You should have a really good answer to that why. Conversely, not every metric _has_ to be a core metric. Just at least one.
- If you know specific goals (grow by X%, slow tickets by X%, cut spend by X%, etc.) it would be good to list them here. It can be very difficult to set specific goals but it can also be okay to set specific goals and then move the goal posts if you're off by orders of magnitude. It's good to document your expectations and thinking as you go.
- Sometimes utilization isn't the actual thing you are looking for. It's okay to have people try something, like it, and then move on. A good example could be [Kompose][kompose], a tool that takes [Docker Compose][compose] files and makes them Kubernetes-ready. In theory a user could use it once, have it convert their Compose file to a Kubernetes config, and then never use Kompose again as the user is now using Kubernetes and growing in that direction. I would argue this perhaps the most successful outcome for this project but if your success metric was "people use this a lot" it would look like a failure.

### Rollback Criteria

I encourage you to think about "when do we stop trying on this." It's a good thought process to go through. Some projects you can just turn off, some you can just ignore if they don't work, some projects you can do a bit of work to undo them, and some projects will be "trap door decisions."

> **Trap door decisions**: a decision that once you make it you can't go back. A good example could be deciding to build your app with React. It's a bit of a trap door because if you later decide to use Angular it requires a total app rewrite which usually means it's a non-starter.

Identifying what it means to unravel a project is helpful and helps you recognize your ongoing cost after a project is released. Features that you launch have a cost and where possible I would urge you to experiment with news and rip out the things that don't work. Your rollback criteria will say something like "if we see low utilization and high churn we will spend a sprint disabling this feature" or something like that. It is typically a good idea to put a date on these: "we will look at these metrics in six month and make a call." If you say, go ahead and just schedule a meeting so you don't forget.

### Timelines

This is answering the question of when. When you do expect what workstreams to happen and when do you expect to have an alpha, a beta, and the general release of your feature. If a project is large enough, you may have milestones here where you describe checkpoints of releasing parts of the content. Generally someone should be able to see when they can expect to see designs, prototypes, and releases at a glance from this sections. Tables, graphs, or some other visual representation is welcome here.

### Designs and Mocks

Anything you can put here to help someone _see_ what you are doing is helpful. Drawings, designs, mocks, charts, graphs, emojis, any sort of visual representation. This can really drive home what people are getting from this product spec.

My favorite and usual way of doing this is browser hacking (since I usually work on web properties.) I will open the project I'm working on in a browser and then edit the HTML and CSS to look like I want it to. Having been a frontend developer this is a very fast activity for me; lean into understanding and speed. It does not need to work, it does not need to be pretty, and it can be hand-wavey. You just want to give people the gist of what you want to do.

Where browser hacking doesn't work I have taken screenshots and photoshopped them, particularly when it comes to iOS and Android apps since I'm not great at Kotlin or Swift.

When that fails, I will usually use Google Drawing. If I need a bit more fidelity I will make a wireframe with Balsamiq. This is usually way too much fidelity (and therefore time) for too little benefit so I only do this when I am really trying to drive home a point. You just want to get your point across, not be a product designer. It's okay if it's 💩-y.

If designs already exist for your project, just link them here instead.

### Technical Concerns and Outstanding Questions

Nearly always when you start projects you will still have big open questions. You do try to close these before you get to reviewing this product spec with folks but frequently there will be questions that just cannot be answered before you start getting into the weeds of implementation. This is the place to call those out. I find that helpful because it often aids in the finding of the answers. Someone can say "oh hey this is how you do that" and save you a bunch of work and can also say "this is so much worse than you think it is" and you can pivot or even scrap the project before you waste your team's time.

Some caution here: I only list what I call _big rocks_ here. A big rock is a large, hard problem that is hard to move. This is not the place for small issues. If your outstanding questions section is massive, it can make your project look like it is more difficult than it is. Really only list issues here when they are big, pose risk, and it is worth calling attention to.

### Appendix

This is everything else. The above sections can't encompass every possible thing you will need to put into a spec and this catch-all at the end is helpful to capture things pertinent enough to call attention to but doesn't fit neatly in any other section I've talked about.

Very frequently I will write _other_ docs for these sections and I will just link them here. Anything you can do to keep your spec shorter means more people will finish it.

[kompose]: https://kompose.io/
[compose]: https://docs.docker.com/compose/
[balsamiq]: https://balsamiq.com/
