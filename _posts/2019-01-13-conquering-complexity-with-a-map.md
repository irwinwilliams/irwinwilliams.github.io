---
title: "Conquering complexity with a map"
date: "2019-01-13"
categories: 
  - "cloud"
tags: 
  - "application-insights"
  - "azure"
---

Last year, I worked with a researcher to develop a really cool, complex Azure solution to augment her work flow with some data. She needed to ingest a large volume of data, clean it up, run some AI on that and then present it. Typical data science activities that she wanted to run in the cloud.

I implemented the flow using several components including Azure Container Instances, Event Grid, Azure ML, Cosmos DB and Azure Functions. My daily drive at work doesn't necessarily let me play in all those spaces at once, so I felt really glad to see all of those pieces work together.

Deploying took a bit more work as I wanted to make that as straightforward as possible. Thus, I used the Azure Fluent SDK that I was fanboying about across a few posts in 2018.

After everything was deployed though, I found visibility into the system was a bit of a stretch. My researcher colleague wanted to easily know where things were at in a given iteration of the process. I didn't have a lot of solutions for that, so it was mostly email alerts.

That is, until I learnt about Azure Application map from two of my colleagues at Teleios - Ikechi, in Ops and Anand in Engineering.

It's a part of Application Insights and lets you track dependencies between various services in an Azure solution. So, just out of the box, you can view the success of calls between web sites and web services and databases and other components. Going further, you can even add other components and dependencies to your app. That got me thinking. Maybe I can use Azure Application Map to display the various components of the solution and track issues in a visual, at-a-glance way?

[I'm going to check it out](https://irwinium.wordpress.com/2019/01/20/making-a-map/).
