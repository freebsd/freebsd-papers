---
layout: slides
title: "Managing Jails with Ansible: A showcase for building a container infrastructure on FreeBSD"
date: 2019-05-18
author: Albert Dengg
email: albert@fsfe.org
youtube: FUxdm4rdrf8
---
Nowadays container technologies like Docker are the first thing you here when the question on how to deploy and manage (micro) services. However, FreeBSD already has lots of features out of the box that can be used to implement lots of the wanted characteristics, but there is still a need for glue code to integrate it into a complete solution.

Ansible is a powerful configuration automation and management system that has a relatively low set of initial requirements. It uses mostly python and ssh, of which the later is needed in most cases anyway to be able to remotely manage the systems. This means that not only the overhead is comperativly low, but also it does not have too many dependencies that will break over time with things like new software releases.

Utilizing the flexible template engine and already available modules to manage features like ZFS, firewall and jails.conf, we will be able to automatically deploy a system that includes

* creating read only templates for service jails
* configuring the network
* configuring the firewall
* creating (multiple) running service jails from these templates
* duplicating jails
* scripting the upgrade & restart of the base and service jails

With that the talk will show how host multiple managed, partly customized applications for multiple distinct user groups with minimal overhead for managing updates and setup of new instances.