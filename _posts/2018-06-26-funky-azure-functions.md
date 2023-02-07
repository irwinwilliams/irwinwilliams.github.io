---
title: "Funky Azure Functions"
date: "2018-06-26"
categories: 
  - "advocacy"
  - "cloud"
coverImage: "impact_sprinkler_mechanism_21.jpg"
---

Let's talk about watering plants.

When I was younger, in my family, I was assigned the task of watering the flowering plants around the house. Thinking back on it now, there was easily 50 plants of all shapes and sizes. So, I would have to shuffle around the yard, bucket in hand, dipping and watering. Some plants would get two dips, others one. I couldn't use the hose, because that might damage the roots of the younger plants. I hated it.

Ever the creative, I used to come up with outlandish ideas to solve the predicament. Sadly, I never implemented any of them. Thus, I was left to water these plants by hand.

Last week, for [Caribbean Developer Week](http://www.developerweek.caribbeandevelopers.org/), I came up with [a demo](https://www.youtube.com/watch?v=mM8jWNs4vWM), featuring Azure Functions, that is the nearest to a solution to my plant watering needs back then that I have ever come.

I built three Azure Functions:

1. Setup Waterer
2. GuidEnqueuer
3. Plant Waterer

Setup Waterer actually created more Azure Functions. Those would be Timer functions, each potentially able to run their own schedule.

GuidEnqueuer, alas poorly named, but good at pretending to be a plant food source, would receive an Http post and enqueue it. Plant Waterer would pick this up and display on a console. No actual plants benefited from this demo.

As I gushed [previously](https://irwinium.wordpress.com/2018/05/07/cloud-fluently/), I created the Setup Waterer function on top of the Azure Fluent SDK and it worked fine. Functions making functions. That's what I wanted to show really, and things worked well.

The code is available on my repo [here](https://github.com/irwinwilliams/FunkyAzureFunctions).
