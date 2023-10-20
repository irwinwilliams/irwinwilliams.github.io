---
title: "Yep. \"Non-Functional Requirements\" is a dumb term."
date: "2023-09-28"
tags: 
  - "software-engineering"
---

Listen to Dave Farley's video below:

https://www.youtube.com/watch?v=4aHKsolzCv4

When I saw his tweet and the title of the video, "Non-Functional Requirements" are STUDID I smiled, favorited his tweet and pinned it in my mind to return to the ideas. I was in a discussion recently about developing regional standards around the role of a Software Engineer.

My colleague and I were reviewing a proposal and the term "Non-Functional Requirements" came up. My role was to validate terminology, principles, ideas and philosophies expressed in the proposal for the Trinidad and Tobago context. The note I shared to my colleague was close to "No... we don't call it that, and don't think about those things in that way".

Really, the things called Non-Functional are often critical quality attributes of the system. I don't know how come it's taken so long for more noise to be made, but those things should definitely not be thought of as Non-Functional. It creates such a dissonance.

Often, it teaches engineers to see those requirements as afterthoughts, consider them some time after you've done the "Functional Requirements". In my experience, things considered "NFR" have led to whole rewrites, either due to security, scalability, reliability or other concerns.

My team and I settled on a borrowed term to give the consideration its appropriate prominence - Quality of Service Attributes. The list varies in size based on specific context, but it feels much more apropos to what we're trying to do, which is build with those attributes in mind, and drive the entire software engineering activity in the right direction from the start.

When writing software, considering quality of service (QoS) attributes is crucial to ensure that the software meets user expectations and performs reliably.

I'm listing a few here for reference:

- Performance: This attribute relates to the software's speed and responsiveness. Users expect software to perform tasks quickly and efficiently.

- Reliability: Reliable software operates consistently without unexpected crashes, errors, or data corruption. It should provide a high degree of uptime.

- Scalability: Software should be designed to handle increased workloads gracefully. Scalability ensures that the software can grow to meet higher demands.

- Availability: Software should be available for use whenever it is needed. High availability minimizes downtime and ensures accessibility to users.

- Security: Protecting user data and system integrity is paramount. Software should have robust security measures to prevent unauthorized access, data breaches, and cyberattacks.

- Maintainability: A well-structured codebase and documentation make it easier to maintain and enhance the software over time. This attribute ensures that updates and fixes can be implemented efficiently.

- Usability: User-friendly interfaces and intuitive workflows are essential for user satisfaction. A software application should be easy to learn and use.

- Compatibility: Software should work seamlessly across various platforms, browsers, and devices to reach a broader user base.

- Scalability: As user demands change, the software should be able to scale to meet those demands. This includes horizontal scaling (adding more servers) and vertical scaling (improving the performance of individual components).

- Resource Efficiency: Efficient resource utilization, such as memory and CPU usage, is important for cost-effectiveness and environmental considerations. Optimizing resource consumption can also lead to better performance.

These QoS attributes should be considered throughout the software development lifecycle, from initial design and architecture to testing, deployment, and ongoing maintenance. Balancing these attributes appropriately is essential to delivering high-quality software that meets user expectations.
