Armed with some stats and graphs, let's chat about metrics. Metrics should be the numerical manifestation of what an outcome looks like to you. Is success a lot of people signing up? Is success less support tickets? Is success making users have to click less to achieve their intents? All of your product goals, planned features, and anything else you do and plan as a PM should manifest itself as changes in metrics. It's how you measure you and your team's success and validate you are doing the right things.

## Team / Organization Metrics

If your team and/or organization does not have top level (often called "North Star" because they guide you) metrics, now is a good time to change that or at least clarify what they are for yourself. These are the metrics that _everyone_ should be working towards and anything that drives me these up should be worthy of working on and anything that _doesn't_ somehow affect these metrics should be strongly questioned.

Let's look at Netflix. What do you think there top level metrics are?

- Sign ups: getting new people in the pipeline is always the goal
- Retention: once someone signs up we want to keep them
- Revenue: if we can get a person to sign up for a higher tier (and have them be happy about it) we should do that
- Watch-hours: people who use our great product are more likely stick around

I'm sure they have more (they did when I was there) but these are some pretty basic ones that most anything else will end up affecting these ones anyway e.g. if we drive down support tickets in theory we should be retaining people better because people with support problems tend not to be happy.

So now your organization has key metrics to follow. Your _team_ should have goals and metrics that then affect the company metrics. So let's say you work on the sign up process for Netflix (I did!), what would your key metrics be?

- Sign ups: duh
- Time to sign up: if a user has the intent to sign up, how fast can we get them from zero to done?
- Bounce rate: A high bounce rate would indicate that we are losing people who would sign up but are hitting a snag somewher
- 30 day retention: signing people up just to churn them later isn't great. It means that they might be surprised by something like cost, a lack of a feature, or something else we could educate them with in the sign up process.

These are just some off the top of my head. But then your team's charter metrics then make sense in the context of company goals which should always be the case. If it doesn't it means either your company's metrics aren't right or yours aren't.

## Project Metrics

It stands to reason then that any project you undertake should affect your team metrics. Whenever I start a new project, I generally write down the problem I'm trying to solve and then the metrics used to measure if we are going to be successful or not. If possible I will make a little dashboard for each project so I can keep track that our projects are successful or not.

So imagine you are starting a new signup project for Netflix. You are going to stop collecting zip code information during the credit card credentials process. If you don't know, it's not required to get the zip code but if you do then you get slightly cheaper fees and certainly less fraud. However it will be even faster (in theory) for people to sign up and that means less bounce. So our metrics for this project would be

- Sign ups
- Time to sign up
- Bounce rate
- Revenue

In this project, we would also want to have a very clear rollback criteria. If we are not signing people up at a larger rate then we would want to roll this project back because it would affect revenue adversely.

## A note on CSAT

CSAT is a metric a lot of companies measure that means customer satisfaction. It will be measured a variety of ways but it usually is some survey or form that is thrust in front of users at some point. It _is_ a good thing to track and you should generally monitor its status over time but careful not overindex on it.

It is a relative metric in that it is relative to itself. If you are measuring customer satisfaction with the sign up process, paying for stuff isn't fun ever. Neither is filling out forms. The best you can hope for is "not painful" when a user evaluates your product. Compare that with the team that does the video watching. They genuinely can hope for "I love this product so much" in their feedback. Imagine sign up was a 4.1/5 and the video watching team got a 4.9/5. Should we be mad at the sign up team? No, not at all because comparing the two doesn't make sense. However, if the video team's metric slips to 4.8 they should care about that and the sign up team should celebrate getting to 4.3. They're relative to themselves.

> Even when I was managing SDKs I couldn't compare across languages. Java developers consistently lowly rated our (and basically every SDK) because they're just salty folks. Whereas we had serious issues with the Node.js SDK and we still got high marks from them. It's always contextual to the demographic.

Therefore be careful making CSAT a focused-upon metric. Track it, absolutely, but recognize its weaknesses. It's not useful to look at by itself. Driving up sign ups while not affecting CSAT is a huge win. Things like that.