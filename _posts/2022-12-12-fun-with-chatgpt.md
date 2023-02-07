---
title: "Fun with #ChatGPT"
date: "2022-12-12"
categories: 
  - "ai"
tags: 
  - "chatgpt"
---

Or, how quickly can you mock up a demo in ChatGPT?

[![](https://irwinium.files.wordpress.com/2022/12/optical-illusions-toroid.gif?w=498)](https://irwinium.files.wordpress.com/2022/12/optical-illusions-toroid.gif)

The morning of my presentation for [DevFest 2022](https://gdg.community.dev/events/details/google-gdg-port-of-spain-presents-devfest-caribbean-2022-port-of-spain/), a friend of mine shared that gif on Facebook. I was curious as to how quickly I could build something like that in ChatGPT.

I literally prompted my way to success, in a few, somewhat poorly worded commands:

1. Using threejs create a 3d animation of a mobius wheel. Give me a sample of this look like in code. Let the rotation to occur within the frame of the browser window. rotate around the center of the renderer, reduce the size of the strip to be 60% of the screen, make the line color silver.

3. Change the texture of the strip to be transparent

5. Make the texture of the strip be like a wire mesh

7. Embed within the strip glowing stars

9. Combine this code with the previous mobius strip code

11. Don't rotate the whole scene, only rotate the strip, make the stars blink, make the strip have a mesh texture

Eventually, it led to [this](https://starr-labs.github.io/ChatGPTJourney_Mobius/).

[![](https://irwinium.files.wordpress.com/2022/12/image-1.png?w=1024)](https://irwinium.files.wordpress.com/2022/12/image-1.png)

Which, LOL, rotates the entire scene, as opposed to just the wheel. But gosh, was it fun.

With a few more prompts, I expect I could get the wheel to spin, instead of the whole world 🌍.
