---
title: "Jumping over hurdles to get to insights using Azure"
date: "2019-04-27"
categories: 
  - "cloud"
tags: 
  - "azure-sql"
  - "global-azure-bootcamp"
---

On the way to getting some data to an Azure DB, I explored strategy in using entity framework that was such a cool timesaver, I thought I'd share it for #GlobalAzureBootcamp

I could have done this years ago. It's just that sometimes a task feels so complex, daunting or mind-numbingly boring that you make do with alternatives until you just **have** to bite the bullet.

We work in SMPP at Teleios. It's one of the ways you can connect to mobile carriers and exchange messages.  From time to time, we need to analyze the SMPP traffic we're sending/receiving and typically, we use WireShark for this. That's as easy as setting it up to listen on a port and then filtering for the protocol we care about. Instead of actively monitoring with WireShark, we may at times use dumpcap to get chunks of files with network traffic for analysis later on.

What we found was that analyzing file by file was tedious, we wanted to analyze a collection of files at once. We'd known of cloud-based capture analysis solutions for a while, but they tended to focus on TCP and maybe HTTP. Our solution needed to be SMPP-based. So, we decided to build a rudimentary SMPP-based database to help with packet analysis.

That's where the mind-numbingly boring work came in. In the SMPP 3.4 spec, a given SMPP PDU can contain 150 fields. The need for analysis en masse was so great that we had to construct that database. But this is where the ease of using modern tools jumped in.

I got a list of the SMPP fields from the WireShark [site](https://www.wireshark.org/docs/dfref/s/smpp.html).  In the past, I would have then gone about crafting the SQL that represented those fields as columns in a table. But now, in the age of ORM, I made [a class in C#](https://gist.github.com/irwinwilliams/66ee09b9c2504f3e25f4f41ab5a719c8). And if you're following along from the top, I created a project in Visual Studio, turned on Entity Framework migrations and added a DataContext. From there, it was plain sailing, as I just needed to introduce my new class to my DataContext and push that migration to my db.

It probably took me 30 minutes to go from the list of 150 fields on WireShark to being able to  create the database without the necessary tables. Now, where does Azure come into all of this?

Each capture file we collect could contain thousands of messages. So, in my local development environment, when I first tried to ingest all those to my database, my progress bar told me I'd be waiting a few days.  With Azure, I rapidly provisioned a database and had it's structure in place with this gem:

> Database.Migrate();

That is, from the Entity Framework DataContext class, I called the Database.Migrate() method and any newly set up db would have my latest SMPP table. From there, I provisioned my first 400 DTU Azure SQL database and saw my progress bar for ingestion drop from days to hours.

With a database that size, queries over thousands of rows went by reasonably fast and gave us confidence that we're on the right path.

We're also working on a pipeline that automates ingestion of new capture files, very similar to what I did [last year](https://irwinium.wordpress.com/2019/01/20/making-a-map/) my Azure Container Instances project.

So, for #GlobalAzureBootcamp 2019, I'm glad that we were able to step over the hurdle of tedium into richer insights in our message processing.
