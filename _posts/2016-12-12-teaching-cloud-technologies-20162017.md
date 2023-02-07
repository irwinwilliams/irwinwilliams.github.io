---
title: "Teaching Cloud Technologies (2016/2017)"
date: "2016-12-12"
tags: 
  - "azure"
  - "cloud-technologies"
  - "teaching"
  - "uwi"
---

We just concluded another run of the Cloud Technologies course at the University of the West Indies. This course is part of the MSc Computer Science program.

As lecturer, I had to come up with the course outline as well as the content. In so doing, I get the opportunity to refresh what we talk about as well as how we approach assignments.

This course comprised of ten modules:

1. Intro to Cloud Technologies
2. Cloud computing infrastructure
3. Virtualization
4. Big data
5. Cloud development patterns
6. Cloud resource management
7. IaaS Automation
8. Microservices
9. IoT
10. Cloud for Research

Though our primary cloud platform is Microsoft Azure, students are free during assignments and project submission to use other cloud providers.

One of the assignments involves virtual machine scale sets and containers. The draught goes like this:

> Z. Zanko Systems provide sales processing systems for large commercial banks.
> 
> They receive more than 5 million JSON requests per hour (revised to 300,000). Each request must be stored in permanent storage. The format of the request is: "{"TransactionID":"1","UserId":"A1","SellerID":"S1","Product Name":"Financial Trap","Sale Price":1000000,"Transaction Date":" "}"
> 
> You have been hired as a System Developer by Zanko. You have access to VMs whose capacity is equal to that of A1 VMs in Azure IaaS or Containers of similar capacity.
> 
> Develop a mechanism to generate the requests your system faces.
> 
> Design and implement a solution using a container-based approach or a virtual machine-based one to process 5 million requests in an hour. For your receivers introduce a failure rate. Store the occurrence of failures. Justify how you chose to store and monitor failures.

Though most students can build this out using azure, one enterprising student chose to use AWS and reading his submission was a nice view of getting this done using Amazon's resources vs Azure.

This year, Microsoft put a halt to the Azure for Education Academic grant, but did have a number of other ways for students to get into cloud, including [DreamSpark](https://azure.microsoft.com/en-us/pricing/member-offers/imagine/) and [other offers](https://azure.microsoft.com/en-us/pricing/member-offers/).

The project component this year changed a bit, too. In the two years prior, we asked students to build working cloud services themselves. This year, we asked them to propose a cloud service that featured understanding of:

- Cloud service definition
- Cloud service models
- Cloud delivery models
- Cloud for research
- Cloud development with a regional focus

We saw some excellent solutions that we hope to hear more about in the future.
