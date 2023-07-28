---
description: >-
  Learn about prioritization methods for product managers, including the
  Complexity vs Business Value matrix and the RICE Method. These frameworks help
  assess the impact, risk, and cost of tasks, allowing you to prioritize
  effectively.
keywords:
  - product manager prioritization
  - prioritization methods
  - complexity vs business value matrix
  - RICE method
  - impact risk cost
  - product management frameworks
---
You will always have more work than you could ever possibly do. I have never met a PM that said "oh cool we are totally out of things to do." You will have more ideas, more features, new products, more tech debt, etc. to work on.

So then a question becomes how to prioritize the right thing to work on. Frequently it is just obvious: X is mission critical, Y is almost done so let's finish it, or Z is on fire and we have to fix it. But sometimes it's less obvious: you have tasks V and W and they roughly seem to be equal priority. What do you do?

Ultimately we are trying to judge three things: impact, risk, and cost. Impact is the rolled up idea of "how deeply is this going to affect how many people?" If you don't migrate the database is your server going to overload and crash? That's high impact. If you add support for an obscure language to your app how many users are you going to affect? Might be a lower impact issue. Risk is the idea of how likely is something to happen. If you don't immediately update your Kubernetes cluster you're probably in a pretty low risk state if it's been updated fairly recently. But if it's never been updated and it's on a beta release? Yeah, pretty high risk. And then cost is how much it's going to cost you from a people and resource perspective. Some things can be low cost high impact like adding an extra button that everyone has been asking for. Other things can be high cost low impact like adding obscure languages support to your app.

Generally those are my preferred terms for thinking about prioritization. That said let me show two more frameworks for ranking things.

## Complexity vs Business Value matrix

![Impact vs Effort matrix](/images/impact-matrix.jpg)

More or less what I was saying above but splits risk into effort and impact. This fairly simple method has you go rank everything by effort (how hard is this to get done) and business value (what sort of benefit does this offer back to the company). 1 being most business value and 1 being least effort. You then go back and add those together and it will give you a relative ranking. I wouldn't take the results as gospel but it does force you to break some ties in your head which can be useful. Sometimes it will become clear "oh this is both low effort and high impact, let's do that."

## RICE Method

This is a method that [Intercom invented and shared on their blog][intercom]. If I am really having a tough time or I am doing group planning where people can't agree I will reach for this as it's the best prioritization framework I have come across. RICE stands for

- Reach: how many people would this affect. Helps avoid you saying "I would use this so it's impactful." Measure in people/quarter typically, but could be something else depending on what you're reaching.
- Impact: A scale value for how impactful something will be. 3 for massive, 2 for high, 1 for medium, .5 for low, and .25 for minimal.
- Confidence: how confident are you in your reach and impact numbers. 1 for high confidence, .8 for medium, and .5 for low.
- Effort: how many people will be working for how long to ship this. Measured in people-months. So if a project needs 3 devs for 2 months, it's a 6 on effort.

Once you have set numbers for these, the formula is (reach * impact * confidence) / effort. That is your RICE score. You then compare all of these to get your priorities.

So if a project affects 100,000 users, is high impact project, has medium confidence, and takes 5 developers 2 months, or  10 person-months, your RICE score would be 16,000. You then rank your proposed projects by their RICE scores and see what bears out as the best thing to work on.

Here's a fun exercise: take your last roadmap for your team and run it through this. Did you all end up with something close to how RICE would have ranked it? If not, why do you think you deviated?

Again, this is not gospel that you must rank by RICE. It's a tool for discussion and unloggjamming your brain when you can't decide between two tasks.

[intercom]: https://www.intercom.com/blog/rice-simple-prioritization-for-product-managers/
