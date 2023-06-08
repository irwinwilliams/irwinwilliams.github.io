---
title: "Running cattle"
date: "2023-06-08"
categories: 
  - "cloud"
  - "running"
tags: 
  - "cattle"
  - "kubernetes"
---

[![](https://irwinium.files.wordpress.com/2023/06/image-7.png?w=1024)](https://irwinium.files.wordpress.com/2023/06/image-7.png)

_Not shown: the other cow who ran away._

The first cow was reticent. And I wasn't enthusiastic about the picture either. I don't really like to stop when I'm on these runs. But to come upon not one, but two bovine beauties on this more-tiring-than-usual run was enough cause to pause.

[![](https://irwinium.files.wordpress.com/2023/06/image-8.png?w=1024)](https://irwinium.files.wordpress.com/2023/06/image-8.png)

Both animals were happily chewing the cud, but with my interest, the first one retreated into the bush, and me, having been lost in said bush just a few months ago, felt no inclination to pursue the matter. The second one, also looked a bit bolt-ish, but I learnt my lesson quickly. I kept the distance, and was thusly rewarded with the cow-fie.

Honestly, cattle had been on my mind prior to this run for completely different reasons, and so this behavior felt incredibly familiar.

If you're into software development you might have heard the adage, "treat your servers like cattle, not pets". When I first heard it years ago, the explanation made sense. It relates to how you think about servers when you are deploying them at scale. That is, try not to think about the individual nodes, say in a cloud deployment, but instead consider the configuration you want, the way you want any node to operate in general and ensure you design a system such that if one instance fails, it can be replaced easily by providing the appropriate configuration.

That's an oversimplification. A much better take on it can be found [here](https://geektechstuff.com/2021/06/24/devops-what-does-cattle-not-pets-mean/).

I was specifically thinking about that tech because I decided to spend more time learning about orchestration with Kubernetes - a common technology used for large scale distributed systems. As I started deploying, I found that it takes a while to get to that "cattle, not pets" state. Often, figuring just the right way to arrange my "livestock" so that I can successfully operate in the world I'm moving to.

The first cow running away was icon for a server I was working with that didn't do what the tutorial I was following suggested it would. It was the defiance of trying to match behavior I had seen in a virtual machine with what I expected in a pod. And it was reminiscent of the quirky networking challenges that led to me re-writing bits of my server code.

Like with the second cow, I eventually got the work done, but not before understanding some the specific challenges with the first cow. I think this pets/cattle analogy is nice to talk about, but is much easier said than done.

{% include youtube.html id="mTrSeaWmJ-4" %}

[The cows are ready for the road](https://www.youtube.com/watch?v=mTrSeaWmJ-4).


