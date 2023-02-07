---
title: "GitHub Copilot: A young Jarvis?"
date: "2021-07-26"
categories: 
  - "bots"
tags: 
  - "cloud-technologies"
coverImage: "img_20180102_132531.jpg"
---

I recently watched yet another time travel TV series on Netflix. This time out of South Korea. I forgot the name, so in looking it up I realized that time-travel K-dramas are very much a thing, lol. Anyway, it's called, "Sisyphus: The Myth". It comes to mind because the writers of the show were fond of having characters repeat the quote,

> The future is already here – it's just not evenly distributed
> 
> William Gibson

I mean, for a time travel show, it's fine. And I think they probably got what they were going after since here I am, quoting them, quoting Gibson. But look, I wrote about Jarvis about [two years ago](https://irwinium.wordpress.com/2019/06/14/one-marvelous-scene-tony-jarvis/). Sort of wondering when will that kind of tech be available. Of having a sort of programmatic _au pair_ who would come alongside and help not just with syntax and formatting, which admittedly, has existed for a long time, but with coming up with the actual code based on your intent.

In that blog post, I didn't put a time horizon on it, but I thought, "maybe soonish". This week though, I realized it's already here.

I just got access to the still-in-beta [GitHub Copilot](https://copilot.github.com/).

[![](https://irwinium.files.wordpress.com/2021/07/image.png?w=1024)](https://irwinium.files.wordpress.com/2021/07/image.png)

It's been blowing my mind and I didn't even read everything on the tin, I just dove right in. In following the first example, it involved creating a method to get the difference between two dates:

[![](https://irwinium.files.wordpress.com/2021/07/image-1.png?w=1024)](https://irwinium.files.wordpress.com/2021/07/image-1.png)

First example ... writing a method with GitHub Copilot's help.

Again, I didn't read everything, so I wasn't sure what would happen when I began the method definition, but things fell into place quickly. I typed the "function calculateBetweenDates(" and sure enough, just like I have grown accustomed to with IntelliSense, I saw a prompt.

But, unlike IntelliSense, these prompts weren't based on any methods I had written or that was available in some framework/library that had been loaded. These prompts came from Copilot's body of knowledge.

Now, excited, I wanted to use an example of something I would do from time to time.

![](https://irwinium.wordpress.com/e745ae9d-52df-4324-828a-909626711c6e)

For a lot of my current projects there's a "sign in to your cloud provider" step. So, that's the method I went with. I wrote, "function signInToAzure(" and after a tab, Copilot has inserted the full method.

Playing just a bit more, in the generated method, I noticed the need for _something_ related to the AAD\_AUTH\_URL. So, I started a method, "function GetAzureADAuthUrl" and voila, Copilot understood and gave me the method.

[![](https://irwinium.files.wordpress.com/2021/07/image-4.png?w=1024)](https://irwinium.files.wordpress.com/2021/07/image-4.png)

These are simple examples, but I really dig how it works.

I've got an AFRAME project I wanted to take this on a spin with, so I'll see it in action in more detail, but this is very groovy already.

Now, just like Tony in Iron Man 2, the question of if _he_ should even be the hero, wielding the suit while being the child and prime beneficiary of a massively successful arms company, the moral questions are in no short supply with Copilot. This includes the licenses of the code used to train Copilot, and whether they permit it to exist in its current form.

Nat Friedman, GitHub CEO weighed in on some of those issues [here](https://news.ycombinator.com/item?id=27678354&utm_source=thenewstack&utm_medium=website&utm_campaign=platform), essentially concluding,

> We expect that IP and AI will be an interesting policy discussion around the world in the coming years, and we're eager to participate!
> 
> Nat Friedman, [HackerNews](https://news.ycombinator.com/item?id=27678354&utm_source=thenewstack&utm_medium=website&utm_campaign=platform)

I'm still in experiment-and-play mode with Copilot, observing where the technology goes, but I'm mindful of the arguments about its existence and will keep tracking that.

Here's to Jarvis, he's a teenager now, but already showing promise.
