---
layout: post
title: 
---
# Grid computing simply explained

![https://iamzain.com/wp-content/uploads/2013/10/network-illustration-868x651.png](https://iamzain.com/wp-content/uploads/2013/10/network-illustration-868x651.png)

In a previous pose called [Clustering simply explained](http://www.iamzain.com/blog/clustering-simply-explained) we looked what a cluster was and clustering. Another word/technology that is thrown about and is similar but quite different is grid technology. So let’s have a look.

## **What is a Grid?**

A grid is a bunch of server nodes working together to accomplish a common goal. Grid technology is used to compute complex scientific or mathematical calculations. An interesting example is the [SETI@home Project](http://setiathome.ssl.berkeley.edu/) which aims to determine if there is life out there by analysing vast amounts of data collected via radio telescopes pointing into space. The data that is collected needs to be processed, this requires huge computing resource. SETI (Seach for Extraterrestrial Intelligence) uses a Grid where each node can be anyone’s PC!

A grid usually has a bunch of grid nodes and a grid master. The grid master is like a project manager, it manages successful completion of the overall task by breaking it down into bite-size chucks and getting the grid nodes to complete those chucks and report back. The grid manager can also detect if a grid node is down, what work it was doing and get another grid node to complete that work.

## **What’s the difference between a Cluster and a Grid?**

The main difference is:

- Cluster – Each node in the cluster is designed to carry out the same task i.e. serve a webpage.
- Grid – A large problem is broken into smaller chunks with different nodes in the grid trying to solve different pieces of the puzzle.