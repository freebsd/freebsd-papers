---
layout: paper
title: ULE: A Modern Scheduler For FreeBSD
author: Jeff Roberson
email: jeff@freebsd.org
paper: /_assets/usenix2003_jeff_ule-scheduler.pdf
---
The existing thread scheduler in FreeBSD was well suited towards the computing environment that it was developed in. As the priorities and hardware targets of the project have changed, new features and scheduling properties were required.  This paper presents ULE, a scheduler that is designed with modern hardware and requirements in mind.  Prior to discussing ULE, the designs of several other schedulers are presented to provide some context for comparison.  A simple scheduler  profiling tool is also discussed, the results of which provide a basis for making simple comparisons between important aspects of several schedulers. 
