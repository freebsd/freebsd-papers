---
layout: slides
title: "Implementing NVMe over Fabrics in FreeBSD"
date: 2023-09-16
author: John Baldwin
email: jhb@FreeBSD.org
youtube: 6sSwkUZNqmc
venue: EuroBSDCon 2023
---
NVMe over Fabrics is an extension of the NVMe specification that
permits use of storage devices over a network. It is similar to how
iSCSI permits access to storage devices using SCSI commands over a
TCP/IP network connection. NVMe over Fabrics supports multiple
transports including Fibre Channel, RDMA (both iWarp and ROCE), and
TCP/IP.

The author has been working on an implementation of NVMe over Fabrics
for FreeBSD. The current work includes a simple userspace host
(initiator) using the TCP transport as well as an extension to
nvmecontrol(8) to discover remote controllers. At the time of
submission the author is implementing a kernel-side host using the TCP
transport. By the time of the talk the author expects to have
completed the kernel-side host as well as a kernel-side controller
(target).

The talk will discuss NVMe over Fabrics in general as well as a
description of the implementation for FreeBSD.
