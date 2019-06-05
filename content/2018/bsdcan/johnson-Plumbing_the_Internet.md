---
layout: video
title: "Plumbing the Internet, BSD-style: Building your Internet presence with BSD"
date: 2018-06-09
author: Thomas Johnson
youtube: YMLyhmaUJI4
---
If you have ever delved into the world of BGP routing on the Internet, you know that it can be quite an undertaking. Fortunately, we can utilize BSD and a couple of open source tools to build a solution that will provide high availability and easy management, at a fraction of the cost of commercial solutions. This talk is an introduction to the basics of building a BGP presence on the Internet, and orchestrating it with Ansible.

If you have ever delved into the world of routing on the Internet, you probably know that it can be daunting. You learned that BGP is the protocol used to build the global routing table, but likely discover that every answer leads to two more questions. Bureaucracy and expensive, proprietary solutions are everywhere. BSD can't stop the red tape, but it does offer a fantastic solution for your technical dilemma.

This talk is a whirlwind tour of building an Internet presence in three parts (and an opportunity to learn from my mistakes). Act one is a brief introduction to the BGP protocol, the process to obtain numbering resources, and connectivity. The basics of rigging a FreeBSD host for routing are covered, and the routing daemon BIRD.

Next up is discussion of network design for high-availability, and the FreeBSD/BIRD configuration to make it happen. Setting up one router may be fun, but we're going to want automation. Enter Ansible. After a quick introduction, we'll use it to deploy a live demo of our configuration

Finally, now that we have a fault-tolerant solution; so let's introduce some faults, and see what happens! We'll induce some failures, and watch how our network responds.

Time-permitting, I will wrap up with some discussion of resources for checking the status of your installation. I'll also discuss some more complex tasks, such as multi-site failover, and taking a router out of service.
