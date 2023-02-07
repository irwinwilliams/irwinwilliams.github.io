---
title: "(the) Hansard Speaks!"
date: "2017-01-07"
---

We built a bot at Teleios.

Well, we've built bots before. In fact, one time, we built this amazing one that was over SMS - part of a game called MeggieWars. It was hilarious and fun. Personally, I've been a fan of using messenger platforms to do fancy stuff for a long time. Way back in 2005 my friend, Kevin Weekes and I attempted to use the MSN Messenger api to do automatic translation between IMs using the babelfish web service. We got as far as the semi-finals for the Imagine Cup that year.

\[caption id="attachment\_394" align="alignnone" width="640"\]![378849_10150330509175060_580830935_n](images/378849_10150330509175060_580830935_n.jpg) Irwin and Kevin, Imagine Cup Participants, circa 2005.\[/caption\]

Anyway, we built a bot in our last Teleios Power Hour [episode](https://www.youtube.com/watch?v=nUgN1K_kGoI) for 2016 - [Hansard Speaks](https://www.facebook.com/HansardSpeaks/). I had been thinking about doing something like Hansard Speaks for a least a year. It lets you search parliamentary proceedings (thus the name Hansard) via Facebook Messenger, thus the Speaks. Any text you type, it will search and then it gives you either a YouTube link of the moment it was spoken in the parliament or a link to the PDF containing the passage.

Right now, it works with a snapshot of the Trinidad and Tobago Parliament data from [YouTube](https://www.youtube.com/channel/UCDvTAcd3t8yEAIiM-Ck49lg) and their [website](http://www.ttparliament.org/).

In terms of the tech we used, we put together Azure Media Services - for the media ingestions - with a Lucene Search in ASP .Net  and did the bot stuff using Microsoft Bot Framework.

As the world [goes crazy for bots](http://gizmodo.com/thousands-of-people-are-watching-two-google-homes-argue-1790843285), I hope to build a few more soon.
