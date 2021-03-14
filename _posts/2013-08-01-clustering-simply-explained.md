---
layout: post
title:
---
# Clustering simply explained

![https://iamzain.com/wp-content/uploads/2014/05/teaching-illustration-868x651.png](https://iamzain.com/wp-content/uploads/2014/05/teaching-illustration-868x651.png)

## **What is a cluster?**

A server working by itself is simply just a server or single node.

When you have two or more servers that are designed to do the same thing that act like one single system, this is a cluster.

## **Why cluster?**

1. Resilience – If one of the nodes in the cluster fails the other node/s will take over ensuring minimal or even zero downtime.
2. Scalability – We are physically limited to the number of cores, amount of memory etc that we can pack in a physical server. Why not use multiple servers to split the workload.

## **What types of clusters are there?**

1. Active/Passive – Only one node is doing any work i.e. the active one. The passive node waits and is ready to get to work if the active one fails.
2. Active/Active – All the nodes in the cluster share the workload. If one node goes down the others can pick up the work.

## **How does a cluster work?**

There are two main types of clustering technologies explained very very basically below:

1. Network Load Balancing (NLB) – Active/Active clusters such as Web and Application clusters usually use this type of clustering technology. The NLB device distributes the load to all of the nodes in the cluster. Each node has no awareness of any of the others. The NLB device can see and detect what nodes are working or not and pass work to the nodes that are working.
2. Heartbeat Clustering Technology – Active/Passive clusters such as database clusters usually use this type of clustering technology. Each node has a special bit of software installed that allows all the nodes in the cluster to check up on each other. When the active node fails the passive node notices there’s no heartbeat coming from the active node and takes over.