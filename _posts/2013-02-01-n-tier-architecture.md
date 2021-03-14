---
layout: post
title:
---
# N-Tier Architecture

![https://iamzain.com/wp-content/uploads/2013/03/design-process-illustration-868x651.png](https://iamzain.com/wp-content/uploads/2013/03/design-process-illustration-868x651.png)

A type of client-server architecture. The most common use of multi-tier architecture is the three-tier-architecture. The three tiers of the three-tier-architecture are summarised below:

1. **Presentation/Web Tier:** Usually the servers that provide the UI to the end users sit here. For example a Tomcat Web Server.
2. **Business Logic/Application Tier:** The servers that host the actual brains of the system. Calculations and processing are done here. Data from the data tier is processed and passed onto the layer above to present to the user.
3. **Data/Database Tier:** The data tier includes mechanisms to store data. Usually servers like database or file servers sit here.

The presentation tier communicates with the business logic layer only. The business logic tier can communicate with the presentation tier and the data tier. The presentation tier can not directly communicate with the data tier.