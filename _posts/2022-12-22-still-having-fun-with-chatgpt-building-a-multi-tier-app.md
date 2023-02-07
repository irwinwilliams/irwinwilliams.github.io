---
title: "Still having fun with ChatGPT: Building a multi-tier app"
date: "2022-12-22"
categories: 
  - "ai"
  - "bots"
  - "collaboration"
tags: 
  - "api"
  - "chatgpt"
  - "consoleapp"
  - "cwacon"
  - "dotnet"
coverImage: "chatgpt-cwacon-1.png"
---

This is the prompt I hit ChatGPT:

_Let's build an app to help me keep track of certain bits of technology news. The name of the app will be CWACON: Cloudy With a Chance of News.  
It will be a combination of a browser app to display a summary of the set of news collected, as well as a c# console app to produce the news summaries.  
News will be categorized according to these categories currently:  
PatternWatch  
AIWatch  
ToolWatch  
PodWatch  
SpaceWatch  
PatternWatch categorizes news activities based on whether there are interesting design patterns in terms of software development, UX, web development, front-end development and related content areas.  
AIWatch categorizes news based on if the content is artificial intelligence, machine learning, data science or data engineering  
ToolWatch categorizes news based on if the content is related to software development or software engineering tools.  
PodWatch categorizes news based on whether a podcast or interview on popular media (such as YouTube, TikTok, Twitter, Instagram) has relevant content to software development or digital product development  
SpaceWatch categorizes content based on if it relates to outer space, such as NASA stories, satellite stories, stories about the solar system and other related technologies.  
All news is gathered from various kinds of social media, such as Twitter, LinkedIn, TikTok and YouTube  
The c# console app, written in dotnet 6 is expected to receive a link from a human correspondent to some source, such as Twitter, LinkedIn, TikTok and/or YouTube and scrape the site based on that link to produce a summary or description of the news item, including any media related to the news, such as images, video or audio. When scraped the data should be stored for easy access and presentation.  
The web app, should present a dashboard of news organized by category and week.  
Summarize the features of the solution described thus far._

And then I spent a little under 3 hours wicking the the console app and API together from that description into something executable. The experience was something like exhilarating.

This approach to development is extremely new, and I'm hesitant to talk about the future too far beyond this. But I can see this enabling development to advance leaps and bounds.

Here's a video showing the effort:

https://www.youtube.com/embed/IJeiah9vSh4
