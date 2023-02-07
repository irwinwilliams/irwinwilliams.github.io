---
title: "Back to the Sky: Processing Satellite Data Using Cloud Computing"
date: "2020-07-30"
categories: 
  - "advocacy"
  - "cloud"
  - "collaboration"
tags: 
  - "azure"
  - "data-pipeline"
  - "satellite"
coverImage: "ggis-satellite.jpg"
---

From time to time, I work with researchers on projects outside of the day to day, forms-over-databases stuff. Mind you, I like a nice form over a cool data repository as much as the next guy, but it's definitely cool to stretch your arms and do something more.

So, when Dr. Ogundipe approached me about cloudifying her satellite data processing, I had to do a lot of research. She had a processing pipeline that featured ingesting satellite images, doing some data cleanup, then analyzing those results using machine learning. Everything ran on local machines in her lab, and she knew she would run into scaling problems.

Early on, I decided to use a containerized approach to some of the scripting that was performed. The python scripts were meant to run in Windows, but I had an easier go at the time getting Linux containers up and running, so I went with that. Once the container was in good order, I stored the image in the Azure Container Registry and then fired it up using an Azure Container Instance.

Like a good story, I had started in the middle - with the data processing. I didn't know how I would actually get non-test data into the container. Eventually, I settled on using Azure Files. Dr. Ogundipe would upload the satellite images via a network drive mapped to storage in the cloud. Since I got to have some fun with the fluent SDK in Azure a while back, I used it to build an orchestrator of sorts.

Once the orchestrator had run, it would have fed the satellite images into the container. Output from the container was used to run models stored in Azure ML. Instead of detailing all the steps, this helpful diagram explains the process well:

![](https://irwinium.files.wordpress.com/2020/07/image.png?w=780)

Super simple.

No, not that diagram.

![](https://irwinium.files.wordpress.com/2020/07/image-1.png?w=1024)

The various cloud resources used to process satellite data in Azure.

So, I shared some of this process at a seminar Dr. Ogundipe held to talk about the work she does, and how her company, Global Geo-Intelligence Solutions Ltd uses a pipeline like this to detect locust movement in Kenya or the impact of natural disasters and a host of other applications of the data available from satellite images.
