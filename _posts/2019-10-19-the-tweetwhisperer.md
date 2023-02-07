---
title: "The TweetWhisperer"
date: "2019-10-19"
tags: 
  - "advocacy"
  - "azure-functions"
  - "chatbots"
  - "gdgdevfest"
  - "microsoft-bot-framework"
coverImage: "tweetwhisperer-doingitforthelikes.png"
---

Today is [GDG DevFest 2019](https://devfest.gdgpos.com) in Trinidad. The organizers put out a call for sessions, and I was happy to share one of the ideas that had been rolling around in my head for a while.

![](https://irwinium.files.wordpress.com/2019/10/image-1.png?w=981)

I Facebook in pirate, don't @ me.

**So, here's the TL;DR**: my idea was to take my likes on @Twitter and funnel them into Google Keep. Along the way, I'll automatically categorize the tweets and then confirm that categorization via a chatbot. Simple stuff.

![](https://irwinium.files.wordpress.com/2019/10/image-2.png?w=1024)

So simple, I didn't even use Visio to diagram it.

What I actually did:

### Twitter Likes

I made an Azure Function that would periodically poll my twitter account and get the last tweets that I liked. To do this, I had to create a developer account in twitter to get the appropriate creds. The function was pretty simple:

https://gist.github.com/irwinwilliams/4d6d765b2da6464af2a3fbc6fac00648

### Categorizing Likes

In the [DotNetConf keynote](https://www.youtube.com/watch?v=1xQE2bWkwjo&t=3740) a few weeks ago, I saw an ML.NET demo and I got the idea to use it here, too.

![](https://irwinium.files.wordpress.com/2019/10/image-3.png?w=1024)

ML.Net to build models (easy peasy)

#### All my notes

I pulled all my notes in [keep](https://keep.google.com) to train an ML model. It was very easy, particularly because I used [gkeepapi](https://github.com/kiwiz/gkeepapi), an unsupported library for interacting with keep.

Doing this made me glad that I could think in terms of a bunch of cooperating functions, because the function to extract the notes from keep was written in python, while most everything else is in C#.

https://gist.github.com/irwinwilliams/c02fbba35c6c33a2971b7ff4e64044c6

KeepIt: A function to get my notes from Google Keep

The funny thing is, I didn't _really_ need the model. Most of the things I stored in keep, were in one or two categories - not very good for modelling. I guess I hadn't really realized that. To be honest, I was probably storing things in keep that I had a very high priority on, which turned out to be mostly cloud things. Go figure.

### How the bot will help change things

So, I'm grabbing my tweets, categorizing them based on history and preference and I'm ready to store them, except, as I've shown above, my categorization is whack. Thus, I also made a chatbot, that will take my liked tweets and ask me to adjust the category I've labelled it as.

![](https://irwinium.files.wordpress.com/2019/10/image-4.png?w=979)

TweetWhisperer: Helping me categorize my tweets better.

So, with these three components, a likes-harvester, a categorizer and a chatbot, maybe, I'll get better at returning to these topics that I have an interest in.
