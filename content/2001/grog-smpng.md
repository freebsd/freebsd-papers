---
layout: paper
title: SMPng
date: 2001-07-29
author: Greg Lehey
email: grog@freebsd.org
---
UNIX-derived operating systems have traditionally have a simplistic approach to process synchronization which is unsuited to multiprocessor application. Initial FreeBSD SMP support kept this approach by allowing only one process to run in kernel mode at any time, and also blocked interrupts across multiple processors, causing seriously suboptimal performance of I/O bound systems. This paper describes work done to remove this bottleneck, replacing it with fine-grained locking. It derives from work done on BSD/OS and has many similarities with the approach taken in SunOS 5. Synchronization is performed primarily by a locking construct intermediate between a spin lock and a binary semaphore, termed mutexes. In general, mutexes attempt to block rather than to spin in cases where the likely wait time is long enough to warrant a process switch. The issue of blocking interrupt handlers is addressed by attaching a process context to the interrupt handlers. Despite this process context, an interrupt handler normally runs in the context of the interrupted process and is scheduled only when blocking is required.
