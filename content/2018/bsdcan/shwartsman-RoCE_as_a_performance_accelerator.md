---
layout: video
title: "RoCE as a performance accelerator"
date: 2018-06-09
author: Slava Shwartsman
youtube: h1NyBaPHuyE
---
RDMA (Remote Direct Memory Access) and its RoCE (RDMA over Converged Ethernet) implementation, currently available in FreeBSD, is growing in popularity as a way to transfer large amounts of data with high bandwidth, low latency and minimal CPU involvement. This session will describe the RDMA stack update done in FreeBSD, focusing on the addition of RoCEv2 (Routable RoCE) and complementary protocols. We will also present the performance benefits of RDMA, demonstrating the enhancement of several storage protocols relaying on RoCE transport, starting with what is already part of FreeBSD  iSER, an iSCSI extension for RDMA, and moving on to more opportunities available on other platforms which can be introduced to FreeBSD.

The topics covered here are:

1. Introducing RoCE v2
 * RDMA concepts/what is ROCE - background and benefits:
 * Higher BW
 * Lower latency
 * Better CPU utilization
 * RoCE v2 - Routable RoCE
 * Review recently updated user and kernel space RDMA applications in FreeBSD12.

2. Complementary protocols  “Ethernet as lossless fabric”:
  * PFC - Priority flow control
  * ECN - Explicit congestion notifications

3. RoCE as a storage performance accelerator:
 * iSER (iSCSI extension for RDMA)
 * Samba direct (SMB direct)
 * NVMF
 * CEPH

Mellanox: http://www.mellanox.com/