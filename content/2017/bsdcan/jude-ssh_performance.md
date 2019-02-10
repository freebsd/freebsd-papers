---
layout: slides
title: "Abusing SSH for ZFS and Profit"
date: 2017-06-09
author: Allan Jude
email: allanjude@freebsd.org
youtube: SbDx2rqo_Is
---
## SSH Bulk Transfer Performance Improvements

Are you waxing your NIC trying to make it go faster? ZFS is so fast, but my replication is slow... why?

SSH tries by default to be very responsive, and sacrifices throughput to remain interactive. This is usually what you want, but not always.

We abuse SSH for many things, be in ZFS replication, rsync, ansible, etc. This work describes a number of proposed improvements to OpenSSH to increase the performance of non-interactive sessions used for bulk transfer.

The author describes ongoing development and tuning work to maximize performance of bulk data transfer over SSH. Development includes improvements to the HPN patch sets to resolve problems with dynamic window scaling (both TCP and SSH windows), new functionality to manually specify a larger remote send/receive socket buffer for high latency networks, and development of the new NONEMAC feature. The author also presents detailed benchmarks on the performance tuning required to maximize transfer rates over both local and long-haul networks. A comparative analysis of the performance of various ciphers on modern amd64 hardware is also presented.

With this work, transfers in excess of 15 gigabits per second were achieved using a pair of E5-1650 v3s back-to-back with 40gbps Chelsio NICs.
