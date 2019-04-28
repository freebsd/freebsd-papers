---
layout: video
title: "Improving netdump hardware support and performance with iflib"
date: 2018-06-08
author: Sam Gwydir
email: sam@samgwydir.com
youtube: FuNgy8Ag4DE
---
Kernel coredumps over the network are useful for debugging embedded machines, disk driver and for high memory machines. This talk covers my experience porting netdump to use the iflib framework, debugging with mdb and dtrace and the resulting performance outcomes.

Kernel coredumps over the network are useful for debugging embedded machines, disk driver and for high memory machines. There has been a netdump patch for FreeBSD since the early 2000s. iflib was introduced in Fall of 2017 providing a standarized set of functions for network driver implementation. iflib currently supports most Intel drivers and Broadcom NetExtreme Family cards, with vtnet support and more planned. Porting netdump to iflib gives all drivers that iflib support netdump support. Improving the netdump facility by generalizing it's driver support with iflib will ease supporting new hardware. Improving core dump performance on >= 10G network cards can improve core dump times over dumping to traditional disks.

The following paper and talk describes my experience porting netdump to iflib, debugging with mdb, and improving the netdump network stack flow control.