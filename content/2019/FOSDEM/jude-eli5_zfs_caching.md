---
layout: slides
title: "ELI5: ZFS Caching"
date: 2019-02-02
author: Allan Jude
email: allanjude@freebsd.org
video: https://video.fosdem.org/2019/K.1.105/zfs_caching.mp4
---
## Explain Like I'm 5: How the ZFS Adaptive Replacement Cache works

An in-depth look at how caching works in ZFS, specifically the Adaptive Replacement Cache (ARC) algorithm. Assumes no prior knowledge of ZFS or operating system internals.

ZFS does not use the standard buffer cache provided by the operating system, but instead uses the more advanced "Adaptive Replacement Cache" (ARC).

* What is a cache
 * How most caches work (LRU)
 * Pros
 * Cons
* What makes the ARC different?
 * Recently Used
 * Frequently Used
 * Ghost Lists
 * What makes the ARC Adaptive?
* Access Patterns (How the ARC adjusts over time)
* Compressed ARC
 * Advantages over compressed memory or swapcache
* Tuning for...
 * File Server
 * iSCSI Target
 * Database
 * Hypervisor
