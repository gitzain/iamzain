---
layout: post
title:
---
# Why use N Tier Architecture?

![https://iamzain.com/wp-content/uploads/2013/03/thinking-illustration-868x651.png](https://iamzain.com/wp-content/uploads/2013/03/thinking-illustration-868x651.png)

In a previous post [N-Tier Architecture](http://www.iamzain.com/blog/n-tier-architecture) we looked at what that was. Great we know what N-Tier Architecture is but what is it good for and why should you use it?

## **Scalable**

Each tier can be scaled independently as and when needed.

## **Better security**

It could be argued by separating out the overall system into this architecture provides added security. If the web server get’s hacked your app server and database servers are still secure etc.

## **Maintainable**

In a big company/enterprise you may have various teams looking after different elements of the overall system. For example the Database Team manages the database, the Windows Team manages the OS. The Application Team manages the application. If everything were installed on one box this presents two main problems:

1. If something stopped working it could become hard to identify what change/update by who.
2. Lack of a segregation of duties. This means the application team could potentially have permissions that would allow them to do stuff or have access to data they shouldn’t.

## **No single point of failure**

This basically means, if everything was installed on one server and that server failed the whole system would be useless until that server was repaired or replaced. Separating out the different elements onto their own server decreases the likelihood of this.

## **Reusable**

Because each tier is responsible for a specific function it makes the tier more easier to reuse. For example the database server can be used to host multiple databases for multiple applications.