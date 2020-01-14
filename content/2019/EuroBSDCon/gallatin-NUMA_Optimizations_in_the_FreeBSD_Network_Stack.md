---
layout: slides
title: "NUMA Optimizations in the FreeBSD Network Stack"
date: 2019-09-22
author: Drew Gallatin
email: gallatin@freebsd.org
youtube: GNmeFi3C1Xg
---
This presentation is about optimizations to keep network connections and their resources local to NUMA domains. These changes include:

 * Allocating NUMA local memory to back files sent via sendfile(9).
 * Allocating NUMA local memory for Kernel TLS crypto buffers.
 * Directing connections to TCP Pacers and kTLS workers bound to the local domain.
 * Directing incoming connections to Nginx workers bound to the local domain via modifications to SO_REUSEPORT_LB listen sockets.
 * Drew presents data from real Netflix servers showing an improvement of almost 2x on AMD EPYC (85Gbs -> 165Gbs), and 1.3x on Intel Xeon (140Gb/s -> 180Gbs). He will present data from the Xeon system showing a 50% reduction in cross-domain traffic.
