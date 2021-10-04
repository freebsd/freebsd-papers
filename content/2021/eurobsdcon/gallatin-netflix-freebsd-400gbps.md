---
layout: slides
title: "Serving Netflix Video at 400Gb/s on FreeBSD"
date: 2021-09-19
author: Drew Gallatin
email: gallatin@freebsd.org
youtube: _o-HcG8QxPc
---

In this talk, I will discuss the efforts to serve TLS encrypted Netflix video at 400Gb/s from a single server. This will be a follow-on to 2 talks at the 2019 EuroBSDCon: [Numa Optimizations in the FreeBSD Network Stack](/2019/eurobsdcon/gallatin-numa_optimizations_network_stack/) and [Kernel TLS and TLS Hardware Offload](/2019/eurobsdcon/shwartsman_gallatin-kernel_tls_harware_offload/). I will provide background on the Netflix video workload, and define key technologies such as NUMA, kernel TLS and hardware kTLS.

I will describe encountering bottlenecks such as:

* Memory bandwidth limits for software kTLS
* PCIe issues with hardware kTLS
* NUMA for software vs hardware kTLS

I will present current and historical performance results from at least:

* AMD “Rome” 2nd generation EPYC systems
* AMD “Milan” 3rd generation EPYC systems
* Ampere Altra arm64 systems

**Drew Gallatin**

Drew started working on FreeBSD at Duke in the 90s, and was one of the people behind the FreeBSD/alpha port. He worked on zero-copy TCP optimizations for FreeBSD and was sending data at over 1Gb/s before gigabit Ethernet was generally available. He spent a decade at Myricom, optimizing their drivers. After a brief hiatus at Google, he landed at Netflix, where he works on optimizing the FreeBSD kernel and network stack for content delivery. He worked on the optimizations to serve unencrypted Netflix traffic at 100Gb/s, and then on more optimizations to send encrypted traffic at ever increasing speeds, from 100Gb/s to 400Gb/s and beyond.
