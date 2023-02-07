---
title: "Save (your data from) Endomondo Month!"
date: "2020-11-23"
categories: 
  - "cloud"
  - "tracks"
tags: 
  - "data-pipeline"
  - "endomondo"
---

Heh.

I hereby dub December, 2020, "Save your data from Endomondo" month. Why?

[![](https://irwinium.files.wordpress.com/2020/11/image-1.png?w=768)](https://irwinium.files.wordpress.com/2020/11/image-1.png)

Endomondo's retiring from the game.

So, given this state of affairs, it would be wise to ensure your data on the Endomondo platform is exported to somewhere. I made a request via their site to get all 789 of my workouts from there and a few days later, I got an archive that included this folder structure:

[![](https://irwinium.files.wordpress.com/2020/11/image-2.png?w=240)](https://irwinium.files.wordpress.com/2020/11/image-2.png)

I wanted to do some analysis on my workout data, so I created a really simple ingestion tool that takes the data from the json documents in Workouts/ and inserts them into a SQL Server database.

The tool can be found in this [repo](https://github.com/irwinwilliams/endomondo-json-to-sql/tree/master).

The key thing about this tool is that I had to fiddle with Endomondo's JSON output to get it to play nice with my approach to serialization:

https://github.com/irwinwilliams/endomondo-json-to-sql/blob/master/WorkoutExtractor.cs

I'm not super-proud of it, because it could be very finicky, but it got the job done for my purposes. I deliberately rejected pulling in the available lat-lon data from the runs, because I wasn't interested in it for the moment, but a slight modification to the approach I've taken will accommodate that.

So, I'm glad the data is ingestible now, and I hope to do some cool stuff with it soon.
