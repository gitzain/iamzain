---
layout: post
title: 
---
# How to virtualize

![https://iamzain.com/wp-content/uploads/2013/07/server-illustration-868x651.png](https://iamzain.com/wp-content/uploads/2013/07/server-illustration-868x651.png)

You’re probably reading this because you want to know what virtualization is or how we virtualization. If you haven’t already you might want to read [What is virtualisation?](http://www.iamzain.com/blog/what-is-virtualisation).

So hopefully we know what virtualization is. Now let’s look at how we would do this:

1. We have a physical machine (host machine)
2. The physical machine has an “Operating System” (host OS) like the “traditional architecture” diagram but instead of installing this we install a special OS called a bare-metal hypervisor..that’s the “VMware” bit in the “virtual architecture” diagram.
3. The hypervisor allows us to create virtual machines.
4. We install a guest OS in the virtual machine.
5. We can create multiple virtual machines and have different OSs in those virtual machines.

![http://static1.squarespace.com/static/52acada3e4b0f7406a396747/52acebc8e4b0ee34bfd8b5fc/5713ef8af699bb6d985d59ab/1462573930679/Traditional+vs+Virtual+Architecture.jpg](http://static1.squarespace.com/static/52acada3e4b0f7406a396747/52acebc8e4b0ee34bfd8b5fc/5713ef8af699bb6d985d59ab/1462573930679/Traditional+vs+Virtual+Architecture.jpg)

Traditional vs Virtual Architecture

The guest OS on each virtual machine thinks it is the only OS on the physical server. For all intense and purposes it thinks it is the host OS i.e. the “Operating System” on the “Traditional Architecture” diagram above.