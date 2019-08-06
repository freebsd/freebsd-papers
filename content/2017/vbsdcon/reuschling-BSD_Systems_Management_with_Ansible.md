---
layout: slides
title: "BSD Systems Management with Ansible"
date: 2017-09-09
author: Benedict Reuschling
email: bcr@FreeBSD.org
youtube: nVJAsfgB7xY
---
Traditionally, shell scripts have been used to apply changes to a Unix system in an automated way. As systems became more diverse (OS versions, patch-levels, etc.) and the number of systems a sysadmin to manage typically grows over time, this classic approach is showing some drawbacks. For example, how do you deploy a change across multiple machines simultaneously in a consistent way? Ansible is a system administration and automation tool to help solve these problems. It can deploy ad-hoc commands or complex scripts (called playbooks) in parallel via SSH to multiple machines. It also supports idempotency, which, in a nutshell, means that a change is applied only once, not multiple times and the system state only changes when said change has not been applied before. In shell scripts, this would require a lot of additional if-then-else checks, which increases the maintenance time and effort. With Ansible, this is already built-in and system administrators can make use of it right away.

This talk will give an overview of how to convert shell scripts to Ansible, including tips and tricks for beginners. My examples are based on my own efforts in managing the Big Data Cluster at the University of Applied Sciences, Darmstadt, Germany with Ansible and the journey it took (and is still ongoing). This is a mixed environment with Linux and FreeBSD machines, (although the trend goes towards the latter) and I will show what sysadmins have to be aware of when using Ansible to manage different OSes. Ansible is not perfect and I will elaborate some of the shortcomings at the end of the talk. Beginners who are new to Ansible will get a good introduction to get started using it, while sysadmins will get an insight into how system administration in a university.
