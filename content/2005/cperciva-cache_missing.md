---
layout: paper
title: Cache missing For Fun And Profit
date: 2005-02-24
author: Colin Percival
email: cperciva@freebsd.org
youtube: id
video: optional-link
---
Simultaneous multithreading - put simply, the sharing of execution resources of a superscalar processor between multiple execution threads - has recently become widespread via its introduction (under the name "Hyper-Threading") into Intel Pentium 4 processors. In this implementation, for reasons of efficiency and economy of processor area, the sharing of processor resources between threads extends beyound the execution threads; of praticular concern is that the threads share access to the memory caches.
We demonstrate that thi sshared access to memory caches provides not only an easily used high bandwidth covert channel between threads, but also permits a malicious thread (operating, in theory, with limited priviledges) to monitor the execution of another thread, allowing many cases of theft of cryptographic keys.
Finally, we provide some suggestions to processor designers, operating system vnedors, and the authors of cryptographic software, of how this attack could be mitigated or eliminated entirely.
