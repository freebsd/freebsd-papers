---
layout: paper
title: "FreeBSD - Live Migration feature for bhyve"
date: 2019-03-24
author: Maria-Elena Mihalescu, Mihai Carabas
email: elenamihailescu22@gmail.com, mihai.carabas@cs.pub.ro
paper: mihalescu-FreeBSD_Live_Migration_feature_for_bhyve.pdf
---
When talking about servers and clouds, live migration is one of the most powerful tools that can be used to manage resources that are abstracted by virtual machines due to its small downtime. bhyve, FreeBSD's hypervisor, does not have a live migration feature implemented yet, even though it is a very useful feature for a hypervisor. This paper presents two approaches for implementing a live migration feature for bhyve that use the FreeBSD's virtual memory subsystem. The first one uses a Copy-on-Write mechanism that cannot be implemented due to bhyve memory layout, and the second one uses a dirty page detection mechanism.
