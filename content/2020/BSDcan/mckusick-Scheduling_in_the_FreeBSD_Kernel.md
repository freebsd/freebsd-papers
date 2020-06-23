---
layout: slides
title: "An Overview of Scheduling in the FreeBSD Kernel"
date: 2020-06-06
author: Marshall Kirk McKusick
---
This talk describes the schedulers available in the FreeBSD kernel: the current ULE scheduler, the real-time scheduler, and the historic 4BSD scheduler. It focuses on the design and implementation details of the default ULE scheduler. It also describes the recent changes that add support for the non-uniform memory access (NUMA) configurations of high-performance servers. The talk concludes by reviewing the results of a paper that benchmarked the ULE scheduler versus the Linux kernel scheduler.
