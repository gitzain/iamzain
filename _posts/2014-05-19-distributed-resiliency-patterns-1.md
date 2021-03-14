---
layout: post
title:
---
# Distributed Resiliency Patterns 1

![https://iamzain.com/wp-content/uploads/2014/05/teaching-illustration-868x651.png](https://iamzain.com/wp-content/uploads/2014/05/teaching-illustration-868x651.png)

You may want to brush up on the post about [N-Tier Architecture](http://www.iamzain.com/blog/n-tier-architecture) if you don’t know what that is.

Today we’re going to look at a very basic resiliency pattern. In fact three of them. One for each tier of our classic three-tier architecture.

## **Presentation/Web Tier**

- Single web server in production data centre.

## **Business Logic/App Tier**

- Single application server in production data centre.

## **Data/Database Tier**

- Single database server in production data centre.

This pattern, in fact, has no resilience. If any of the server nodes fails the entire system is useless until that node is repaired or replaced.