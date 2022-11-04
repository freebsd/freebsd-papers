---
layout: slides
title: 'The “other” FreeBSD optimizations used by Netflix to serve video at 800Gb/s from a single server'
date: 2022-09-18
author: Drew Gallatin
youtube: 36qZYL5RlgY
---
### Quantifying the importance of several FreeBSD optimizations to serving web traffic at extreme speeds.		

In previous talks, I've focused on new optimizations such as NUMA and NIC kTLS
offload, which are critical to serve 800Gb/s.  In this talk, I'll focus on the
contributions of older, but equally critical optimizations, such as

- TCP segmentation offload (TSO)
- TCP large receive offload (LRO)
- VM optimizations such as the UMA VM pg cache zone and batchqueues
- Asynchronous  sendfile
- Unmapped (extpg) mbufs

I will briefly describe the importance of each of these unsung optimizations,
explain why they help, and quantify the value of each optimization using a
metric I call percent-CPU per Gb.

I will wrap up by putting them all together and showing results from an
experimental Netflix server serving production traffic at 720Gb/s.
