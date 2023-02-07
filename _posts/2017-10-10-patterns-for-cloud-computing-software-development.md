---
title: "Patterns for Cloud Computing Software Development"
date: "2017-10-10"
---

 

Our text today came from the [Cloud Architecture Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/) from Microsoft. This was our first class on cloud architecture and so we spent time looking at several popular patterns, including,

### Circuit Breaker

I called back to that night I built a website for tracking the St. Joseph By-election in 2015 and how I could have used this on the client side when things became too intense for the database server.

### Compensating Transaction

The writing on this is great, but Clemens Vasters explanation of  [Sagas](http://vasters.com/archive/Sagas.html) really brought this home to the class.

### Competing Consumers Pattern

This is one of the patterns we've used a lot for our messaging solutions at Teleios, so it was easy to walk through and talk about messaging demos featuring it with the class.

### Compute Resource Consolidation Pattern

I used this pattern to start the discussion on how containers are a great way of consolidating a set of compute-based activities. From the patterns guide, there was a great example though of the need for care to ensure that the right kinds of tasks are consolidated. Tasks with dissimilar characteristics can reduce the efficiency gained from pursuing consolidation.

In talking about this pattern, this amazing quote was uttered in class:

https://twitter.com/iStarr/status/917522769184780288

The next assignment is based on Event Sourcing and Materialized Views, where students have to come up with a scenario that features the use of ES and MV and then build a demo that explores their chosen scenario.

It was also cool to see the call back from our big data class last week because I highlighted that Apache's HBase might be a good data store for building a solution involving Event Sourcing.  There's also a [great article](https://www.confluent.io/blog/event-sourcing-cqrs-stream-processing-apache-kafka-whats-connection/) talking about the Command & Query Responsibility Separation pattern in the context of Event Sourcing, too.
