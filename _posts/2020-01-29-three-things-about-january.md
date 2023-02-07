---
title: "Three things about January"
date: "2020-01-29"
tags: 
  - "software-engineering"
---

Just before I went back out to work in January, I had a fair sense of how I wanted to start the year. At work, I'd be diving in to Planner and refining some early 2020 goals that Anand and I had come up with. At projects, I'd be doing some arduino and bot stuff. All great.

But from January 2nd, I found myself very deep in legacy code from at least a decade ago. And I was working very late. It's like time stood still. When my team and I raised our heads for a week, a change to the environment around that same code meant even more speelunking.

Out of this last few weeks I saw three things of note:

try  
{  
//actual code to do something meaningful  
}  
catch  
{  
//empty, meaningless catch block  
}

1. Stop using empty catch blocks.  
    I haven't had cause to leave dangly, useless catch blocks lying around for a few years, but I remembered when I used to. And boy was it a shocker. In the age of amazing tracing tools like App Insights, throwing away trace opportunities was like a slap in the face.  
    When I showed a few developers at work some examples of empty catch blocks, they understood why it might have happened - I didn't know what I wanted to do with the exception at the time - but my response was largely, "well, at least log it na". At least. Even logging took a hit this month.  
    
2. Log with sense  
    The worst kinds of exception message in a log is "An exception occurred". For the most part, sometimes, when looking for the flow of a problem, I might just put a log statement to show that we got to a place in code. Sometimes, that place is an error handler. The way I see exceptions now, if you're logging that it occurred, take some time to log what that block was trying to do, as well as what parameters are available. In a messaging system for example, simply a message Id is a big deal. So, first we log, then we log with sense.
3. Sleep is very good.  
    Not just sleep, but a firm commitment to not rush off with the first good idea you have when facing a problem. I have actually heard this stated another way, "Beware the danger of the first light". While trying to debug our way out of the hole we were in, several ideas came up. Most recently, I had a great one that would have led to massive changes in the system. I was about to announce it, but one of the managers on our team cautioned me. She said it was Friday, sleep on it and see if you feel the same way on Monday.  
    Monday came, I felt the same way. Until I spoke to one of the newest engineers on our team and realized we could achieve what I wanted to with a change to one module, as opposed to the whole system. That was good.  
    Over the course of this month, there were a lot of challenges.
