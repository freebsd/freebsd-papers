---
layout: slides
title: "FreeBSD networking in virtualised hosting — 2021 and beyond"
date: 2021-09-18
author: Patrick M. Hausen
email: hausen@punkt.de
youtube: Tqg2UH6Mvoc
---

This talk will present the current state of networking for FreeBSD based
containers (jails) and virtual machines based on our own experience running a
private hosting infrastructure.

I will present the challenges we faced and solved, like IPv4 address scarcity or
vastly different network architectures across various bare metal providers. And
the ones we are still facing like increasingly large broadcast domains in layer
2 networking, and the ideas we (and others) have about possible solutions and
the future direction of the virtual network stack.

This is an operator’s point of view that references the kernel and userland
implementation but focuses on the use of the various subsystems involved instead
of the kernel implementation proper.

**Patrick M. Hausen**

Patrick M. Hausen, born 1968, developed an interest in “all things Unix” and
networking in general in the late 80’s. Having worked on various commercial
implementations and looking for an operating system that would be more capable
than Minix for actual daily use at home he found out about FreeBSD in 1993. He’s
been using, hacking, advocating and occasionally cursing FreeBSD ever since.
