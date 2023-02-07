---
title: "In media res"
date: "2021-05-24"
categories: 
  - "bots"
tags: 
  - "microsoft-build"
  - "microsoft-teams"
---

I've been playing with an idea in Microsoft Teams for a few months now. It hasn't yet borne fruit, but I've decided its time to move on, and maybe revisit it in a few more months with fresh eyes.

This sort of breaks with how I've considered writing posts on here. I like each post related to a creative activity to represent a singular finished work. I can refine things and come back, but each should say, "I did this and here's the result". But I'm writing about being in the middle of things, largely as an exercise in discipline, but also, as a clear record for myself of what I've done.

So what was it?

Scott Hanselman had this post on Twitter about making credits appear at or near the end of a Teams meeting. From the time he put it up, I was pretty clear on how he might have done it.

https://twitter.com/shanselman/status/1357036562077241344

Genesis of my idea for a Microsoft Teams End Credits bot came from this.

I think apart from the fact that we all become video presenters last year, we also became much more familiar with OBS. And the approach he used could be done with OBS. Which he described [here](https://www.youtube.com/watch?v=-oaikJCR6ec).

In fact, I think I saw an earlier tweet from him about a dude doing essentially a transparent board overlay with OBS, too. OBS to me, feels easy to use, but when you put everything together, it could feel like a bit of work. You have to set up your scenes, fill them with the right layers, and hang everything together, _just so._

So, not hard, but somewhat involved. Since I'd been [experimenting](https://irwinium.wordpress.com/2020/10/19/agents-of-teams/) with the audio and video streams of Teams calls, I could see how a similar thing could possibly be done in Teams directly. Which would let me yell, "Look ma! No OBS!", while achieving the same functionality.

Quite a few of these experiments begin with messing around with a sample, here and there. Call it SDD - Sample Driven Development. I picked up where the [HueBot Teams](https://github.com/microsoftgraph/microsoft-graph-comms-samples/tree/a4c6c6c8ae96cbd0125851dcc64278f9d02328cb/Samples/V1.0Samples/LocalMediaSamples/HueBot) sample left off. It's one that let's you create a bot that grabs a speaker's video stream in a call and overlay it with a given hue - red, green or blue. I'd gotten that to work. And last time I played with that sample, I was able to send music down into a Teams meeting using a set of requests to a chatbot.

Now, I wanted to essentially overlay on a given video stream, the same credits info that I saw from Scott's OBS trick.

I am currently still in that rabbit hole.

Yes, I was able to access the video stream based on the sample. I even got to the point of overlaying text. But pushing that back down to the call for everyone? Various shades of failure.

- ![](https://irwinium.files.wordpress.com/2021/05/blog1-go.png?w=1024)
    
- ![](https://irwinium.files.wordpress.com/2021/05/blog2-go-oversized.png?w=1024)
    
- ![](https://irwinium.files.wordpress.com/2021/05/blog3-go-half-oversized-1.png?w=1024)
    
- ![](https://irwinium.files.wordpress.com/2021/05/blog4-go-third-oversized-1.png?w=1024)
    
- ![](https://irwinium.files.wordpress.com/2021/05/blog5-go-quarterbutactual-1.png?w=1024)
    

The first image is essentially straight out of the sample, where guidance was provided on how to extract a bitmap image from the video stream, which is otherwise formatted in NV12. The other images in the carousel are what appeared in Teams, with various degrees of resizing but always having a blue hue.

https://gist.github.com/irwinwilliams/e00a4fefb4871acd54242ebbb7a4a94d

This code essentially does the transformation.

I'm currently stuck with that blue hue. 😕.

So, since the sample only had a one-way transformation of NV12 to bitmap, not having any experience with that, I speelunked around the web for a solution. Normally that would mean some drive-by \[StackOverflow\]ing for a whole method, but that got me as far as those blue hues.

Literally, the method I got from S/O let me convert BMP to some kind of NV12, but not something that Teams quite liked.

https://gist.github.com/wobbals/5725412

I converted this Java method to c#.

Part of the conversion meant reading up on [YUV](https://wiki.videolan.org/YUV#). The Java method focused on YV12. Teams needed the stream to be NV12. Their differences are summarized here:

> NV12
> 
> Related to I420, NV12 has one luma "luminance" plane _**Y**_ and one plane with _**U**_ and _**V**_ values interleaved.
> 
> In NV12, chroma planes (blue and red) are subsampled in both the horizontal and vertical dimensions by a factor of 2.
> 
> For a 2×2 group of pixels, you have 4 Y samples and 1 U and 1 V sample.
> 
> It can be helpful to think of NV12 as I420 with the U and V planes interleaved.
> 
> Here is a graphical representation of NV12. Each letter represents one bit:
> 
> For 1 NV12 pixel: YYYYYYYY UVUV
> 
> For a 2-pixel NV12 frame: YYYYYYYYYYYYYYYY UVUVUVUV
> 
> For a 50-pixel NV12 frame: Y×8×50 (UV)×2×50
> 
> For a n\-pixel NV12 frame: Y×8×n (UV)×2×n
> 
> FROM: [VideoLan on YUV#NV12](https://wiki.videolan.org/YUV#NV12)

https://gist.github.com/irwinwilliams/316166d9701d04828a140d478a5e007c

Converted the YV12 approach to NV12.

Even though I modified a method's to produce NV12 from a BMP array, no joy. And this after much tinkering..

Eventually, I even tried using the OpenCV project, but that just led to green splotches all over.

Thus, I'm stuck. I still love the idea, but I've poured way too many hours into the experiment at this stage. I'm looking forward to [Microsoft's Build](https://mybuild.microsoft.com/home?wt.mc_ID=iStarr) this week. Maybe I'll find some helpful soul to set me on the straight and narrow.
