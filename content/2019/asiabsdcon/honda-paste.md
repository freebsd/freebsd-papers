---
layout: slides
title: "Doubling FreeBSD request-response throughputs over TCP with PASTE"
date: 2019-03-23
author: Michio Honda and Giuseppe Lettieri
email: micchie@sfc.wide.ad.jp
slides: 
paper:
video: https://video.fosdem.org/2019/K.1.105/zfs_caching.mp4
---
Request-response workloads are common in practice, including key value stores,
RPC and other HTTP workloads. Performance of these workload is largely limited
by system call and I/O overheads, because the application needs to process a
large number of requests arriving at the different TCP connections at the same
time (e.g., notified by kevent), issuing a pair of system calls (e.g., read()
and write()) to each of them. Even worse, inside the kernel, it is difficult to
perform I/O batching across multiple TCP connections. In this talk, we report
how FreeBSD performance can be improved using PASTE that uses netmap(4) API atop
and below the kernel TCP/IP implementation. We show that PASTE improves
throughput and latency by a factor of two; In BSDCan 2018, we introduced
concepts of PASTE but without meaningful performance improvements in FreeBSD.
Finally, we discuss issues we are facing, for example, soupcall() that is not
notified of empty-data mbufs that carry FINs. Implementation and installation
documents are available at https://micchie.net/paste/.
