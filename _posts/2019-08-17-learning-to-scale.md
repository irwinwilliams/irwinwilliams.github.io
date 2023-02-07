---
title: "Learning to scale."
date: "2019-08-17"
tags: 
  - "cloud-technologies"
  - "cxc"
  - "scalability"
---

![](images/image.png)

My friend Christopher shared this on Facebook. It's a queue for CXC results.

Tomfoolery. That's the adjective that bubbled into my mind when I saw this screenshot and understood what it was describing.

Admittedly, this was a bit harsh. I mean, someone built this, they took the time to craft a way to deal with the rush of users trying to get their examination results from the Caribbean eXamination Council (CXC). They (CXC) have a classic seasonal scale problem.

During the year, the number of users hitting their servers is probably at a manageable level. And when results come up, they probably literally see a 10-fold increase of access request. They'd have the numbers, but I think this guess is reasonable.

![](images/image-1.png)

I was curious about the traffic data on cxc.org, so I got this from similarweb.com

Their solution may have been reasonable in 2012, when maybe scaling on the web was more of a step-wise move in terms of resource management than a flexible thing as it is today. Scaling may have meant buying new servers and software and getting a wider team to manage it all.

But there are solutions today that don't necessarily mean an whole new IT investment.

![SAD sporting](images/https%3A%2F%2Fblogs-images.forbes.com%2Fbillconerly%2Ffiles%2F2014%2F12%2FSAD-sporting1.jpg)

I really dig this chart from [Forbes](https://www.forbes.com/sites/billconerly/2014/12/15/seasonality-in-business-and-economics-a-primer/?via=iStarr#2aa07ff47870) demonstrating the seasonality challenge

So, how do you contend with seasonal IT resource demand without breaking the bank? Design your solution to leverage "The Cloud" when you need that extra burst.

"The Cloud" in quotes because if things were as easy as writing the line, "leverage The Cloud" then we wouldn't be this deep on a blog post about it. So, specifics, here's what I mean:

Plan the resources needed. In this case, it might be a solution that uses load balancing where some resource is handled on-prem and capacity from the cloud is used as needed. Alternatively, an whole new approach to sharing the resources at play might be worth investigating - keeping authentication local, but sending users to access results stored in the cloud via a serverless solution is a great consideration.

I don't want to spec out the entire solution in two paragraphs. I do want to say CXC can and should do better, since they serve the needs of much of the Caribbean and beyond.
