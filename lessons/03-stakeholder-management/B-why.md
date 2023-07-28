---
description: >-
  Learn about the considerations involved in making product decisions and their
  impact on stakeholders using examples from Google Maps, such as increasing
  sponsored listings and improving the API. Explore the trade-offs between
  generating more revenue and maintaining a positive user experience.
keywords:
  - product decisions
  - stakeholders
  - Google Maps
  - sponsored listings
  - revenue
  - user experience
  - API
---
Why do we care about doing this first? Because we are building our product for our stakeholders and we need to be mindful that every product decision we make doesn't just affect the users we are targeting but has a ripple effect to all of our users. It can be okay to trade off making something good for one stakeholder at the cost of the another but the point here is to be intentional. Let's make some examples (again using Maps).

### Let's make more money

Let's say we get a directive from management that we need to pull in more money for Google Maps. Take a second here and think about some ideas you would do to make more money on Google Maps.

One idea is to increase the amount of sponsored listings on Maps. Frequently users will search for things like "coffee shop" or "italian restaurant" on Maps and Maps will show preferrential treatment to your business if you pay for it. So an easy path to more money is more sponsored slots. Instead of showing a max of 2 sponsored ads, we could show 5. Bam. Done. Free money.

But let's look at it from a stakeholder management perspective.

- We do help net-new businesses that pay for those listings
- We do harm businesses that were already being shown as sponsored listings; we have diluted the value of an ad by showing more than just 2. An ad now is less valuable and that harms people already giving us money.
- We do harm businesses that don't pay for those listings; when they would have otherwise ranked higher in a search they are being pushed down in the listings because someone paid to jump above it
- In theory, your ranking algorithm is giving back the best results for a user searching for a "coffee shop" but you actively presenting to them something your ranking algorithm has ranked as better. I think it's fair to say you are choosing to present an inferior user experience so you can make more money.

This is actually a real story from me this week. I was looking to buy a bottle of tequila as a gift for a friend on a popular grocery delivery service and so I search for "tequila" from supermarket. This particular service had apparently sold the "tequila" keyword to not just other tequilas (something that would be fine, it's tequila and which order you present them to me is a choice anyway) but to other types of alcohol like vodka, hard seltzers, and bourbons. I counted and of the 20 initial results, 50% were ads and 40% of all results were _not_ tequila but some other type of alcohol. It was a frustrating experience because I had to sift through a bunch of objectively wrong results to find what I was looking for. They sold me out as a stakeholder.

In this situation should you do it? I would argue it is unlikely to increase profits enough to justify how much it adversely affects other stakeholders, but you would need to assess how much it degrades user experience and how much it increases profit. The metrics matter here.

### Let's improve our API

Let's then fathom that we as a Google Maps look at our public API and decide there is some big improvements we can do. We can make it cheaper to run, easier to use, and easier to get started with. Seems like a slam dunk win, right? Let's break it down by stakeholders.

This does benefit new developers to the platform. They get something that is easier to work with and more comphrensible to work with. That is certainly a benefit.

This does benefit internal stakeholders as we get to run a "better" service for cheaper which is a benefit.

This _can_ benefit existing developers using our platform. In theory if they maintain their apps it will be easier going forward but the big problem is that they will have to rewrite existing code that already works to keep up with your churn. Overall I would argue for most developers that is a net negative. Existing code that works is the best. Forcing them to rewrite it because you are choosing new patterns does not benefit them, it benefits you. You are choosing your needs over there's.

Inevitably many developers will not upgrade their apps, either because they don't maintain them actively or because they will choose not to. This will mean that apps that were previously working will cease working which is negative for both the developers but also the end users of those apps.

Another case where you need to weigh all the options. This is a very real problem I faced at Stripe: developers _really_ do not like changing code that deals with money and for good reason: bugs cost real money. Forcing them to rewrite sections is something we took super serious and avoided at all costs. If you wrote a Stripe in 2015 and left it untouched it very likely still works today because of how serious Stripe takes that commitment.

