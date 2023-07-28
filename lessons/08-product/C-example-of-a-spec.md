---
description: >-
  Netflix seeks to add a feature that allows users to watch shows together and
  engage in synchronized video chats similar to FaceTime. The goal is to provide
  a true living room chat experience for users while watching their favorite
  shows, leveraging video-chat-enabled devices.
keywords:
  - Netflix
  - watch shows together
  - synchronized video chat
  - living room chat
  - FaceTime
  - video-chat-enabled devices
---
Let's pretend for a moment you are a product manager at Netflix and your task is to add a feature that allows users to video chat (like Zoom or FaceTime) with someone and watch a synchronized stream of a show together. What would that spec look like before we got started with it? 

Here's how I would write it (where I don't know things I'm just making it up):

# Watch Together Product Spec

## BLUF

Netflix users frequently express a desire to watch shows with friends and family remotely while engaging in real-time discussions. Previous attempts to implement such a feature have not met the desired results. The goal is to provide users with the ability to watch Netflix content together, regardless of their devices, and have a synchronized video chat similar to FaceTime.

## Problem Statement

As a watcher of Netflix shows, I want to be able to watch with a friend the same content at the same time and talk about it.

A feature that Netflix has frequently attempted but has yet to get right is having living room experiences where watchers can chat about a show in progress with their remote friends and family. We have tried just synchronized video, watch parties on Xbox, leaving text notes for future watchers, and more but have yet to see the results we want. Yet it is still one of the most common requests from users.

This feature attempts to put the best of all of these and put them together so that our watches can have a true living room chat about their favorite shows as they are witnessing it together. X% of our users are watching Netflix on video-chat enabled devices and we are going to leverage that as they have a video chat (think FaceTime-like) while watching a synchronized video.

## Goals and Non-Goals

Goals

- Allow two people to watch a show together
- Allow users to watch together regardless of their device as long as it has video and/or audio
- Allow users to watch shows together as long the show is available in both users' region
- Allow users to pause, scrub, and skip shows and have it work for both users
- Allow users to set their own subs and dubs and that can be different for each user

Non-Goals

- Allow more than two users
- Solve for users that don't have video devices
- Encourage users to chat without watching a video

## Key Metrics

- Time spent watching Netflix using Watch Together
- Time spent in chat total
- Users who use this feature within a week of signup: indicates a user may have signed up to use this feature
- Month-over-month retention on feature: indicates users find it useful to use it more than once
- CSAT: after users finish a chat, a one-question survey will ask them how it went. If bad, we will ask why.

## Rollback Criteria

After three months, we will look at initial metrics to see if users of it are rating it well and if they users are using it more than once. If it look good we will promote further and follow up. If it is not looking good, we will meet to see what we can improve. We do this again at six months.

If by nine month we do not see X% growth, X retention, or X CSAT, we will begin winding down the feature.

## Timelines

![Timeline](/images/timeline.png)
<sup>Made with <a href="https://time.graphics/">time.graphics</a></sup>

| **Event**            | **Date** |
|----------------------|----------|
| Product Review       | Sept 13  |
| Beta Release         | Oct 25   |
| General Availability | Nov 26   |

## Mock UX

> **Note**: this mocks the user experience but not the final designs.

User opens their app to the show they wish to watch with a friend. They click on "Watch Together"

![Mock 1, adds a "Watch Together" button](/images/mock1.png)

A show modal shows up. User invites their friend to watch with them and she accepts

![Mock 2, shows a choose contact pop up](/images/mock2.png)

User watchers show with friend

![Mock 3, shows a woman chatting with as you watch a show](images/mock3.png)
<sup>Photo of woman by <a href="https://unsplash.com/@jakenackos">Jake Nackos</a> on <a href="https://unsplash.com/photos/IF9TK5Uy-KI">Unsplash</a><br>Designs belong to Netflix with only minor edits by me</sup>
  

## Outstanding Questions

### Legal

Both users of this feature will have their own independent subscriptions to Netflix and watching distinct streams that function the same. However we need to investigate if the act of synchrony amongst watchers in different places is a legally distinct action according to our contracts with content providers.

### WebRTC, Vendor, or Build-It

We still have no settled on how precisely to stream the video chat. Having nearly the same predictable latency as the Netflix video will be important because if the sync drifts too much it will be annoying to users. WebRTC is preferred as it would peer the connection and therefore cost nothing to Netflix to run. We could also buy an-off-the-shelf solution such AWS Chime. Lastly, we could build an in-house solution to save cost and make the stream the most predictable.

## Appendix

- [Off-the-shelf vendor in-depth investigation](#)
- [What competitors have done in this space](#)
- [Retrospective on what Netflix has tried before](#)
