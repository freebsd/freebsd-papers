---
layout: slides
title: "PASTE: Fast End System Networking with netmap"
date: 2018-06-08
author: Michio Honda
email: micchie@sfc.wide.ad.jp
youtube: y_F-8HijfOA
paper: honda-PASTE_Fast_End_System_Networking_with_netmap.pdf
---
We introduce PASTE, an extension to the netmap framework for end systems to exploit high speed NICs, kernel TCP/IP stack and emerging persistent memory. We describe design and implementation of PASTE, as well as how to write applications on top of it.

New hardware, such as high-speed NICs and persistent memory introduces significant challenges in system software design and implementation. Today's socket APIs are already unable to serve on 10 Gbps under message-oriented workloads. Suppose a server that runs a poll/kqueue event loop to handle concurrent TCP connections. Arriving messages create a long queue of ready sockets where each must be processed by a pair of read/write system calls; If the application is notified of 100 messages on parallel TCP connections, it requires 200 system calls to process this single event, significantly reducing throughput and increasing end-to-end latency. Persistent memory eliminates a bottleneck of disks/SSDs because of 2-3 orders of magnitude lower access latency, which makes the network stack be a bottleneck even when the application persists receiving data. In particular, data copy from socket buffer to persistent memory comes at significant cost.

To solve these problems, we introduce PASTE, an extension to the netmap framework. Unlike the original netmap, it supports TCP/IP in the kernel, yet offering the netmap API to applications for zero copy and batching of system calls and packet I/O, even across multiple TCP connections. PASTE further supports emerging persistent memory, allowing applications to persist data without copying data since NIC's DMA. Applications can form persistent data structures using netmap's packet buffers backed by a file. PASTE was initially implemented in Linux for research purpose and demonstrated notable performance improvements. We are now porting it to FreeBSD. We will report software architecture and performance of our FreeBSD prototype. We then would like to discuss necessary extensions beyond the netmap framework, which include socket structures and NVDIMM supports. With PASTE, we believe the netmap API to be an even more generic, promising networking API of FreeBSD beyond packet I/O framework, and to enable building efficient end systems by exploiting emerging hardware.ls ho