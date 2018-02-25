---
layout: paper
title: Implementing a Clonable Network Stack in the FreeBSD Kernel 
author: Marko Zec
email: zec@tel.fer.hr
---
Traditionally, UNIX operating systems have been equipped with monolithic network stack implementations, meaning all user processes have to cooperatively share a single networking subsystem. The introduction of the network stack cloning model enables the kernel to simultaneously maintain multiple independent and isolated network stack instances. Combined with forcible binding of user processes to individual network stacks, this concept can bring us a step closer to an efficient pseudo virtual machine functionality which opens new possibilities particularly in virtual hosting applications, as well as in other less obvious areas such as network simulation and advanced VPN provisioning. This article is focused on design, implementation and performance aspects of experimental clonable network stack support in the FreeBSD kernel

