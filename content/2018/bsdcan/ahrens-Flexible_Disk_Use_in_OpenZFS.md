---
layout: video
title: "Flexible Disk Use in OpenZFS"
date: 2018-06-09
author: Matt Ahrens
email: mahrens@delphix.com
youtube: oue2cPFK7AU
---
One of the original goals of ZFS was to “end the suffering” of system administrators, by making storage easier to manage. A big part of that is reducing the restrictions on how ZFS can be configured, thus reducing the need for advance planning and investment. This talk covers two new features that further this goal: Device Removal and RAID-Z Expansion. In this talk, you'll learn how these features work under the hood, as well as how to best take advantage of them.

Device Removal decreases the total amount of usable space in the pool, allowing disks to be removed from the system. As part of the removal process, allocated space on the device is copied to the remaining disks in the pool. There are two primary use cases for this:

1. A mistake was made when adding a device to the pool. E.g. the wrong device was added, or it was added as the wrong type.
2. Storage migration. E.g. moving the pool from six 4TB drives to four 10TB drives.

Device Removal is available in FreeBSD CURRENT.

RAID-Z expansion  adding a single disk to an existing RAID-Z group  is perhaps the most-requested OpenZFS feature ever. This feature will make it easy to add small amounts of storage incrementally to modest-sized pools. System administrators will no longer be trapped by their past decisions of RAID-Z group size, forced to continue with a suboptimal RAID-Z stripe size, or rebuild their pool from scratch.

This talk will explore the design trade-offs of RAID-Z Expansion, as well as some implementation details. To give an example: all the data needs to be read and rewritten in the new layout. If there is a disk failure while this is in progress, we must ensure that we can still reconstruct the data, which means that the sectors of each logical stripe must all be on different disks. But with RAID-Z’s variable stripe with, this is nontrivial to ensure, because we don’t know where each logical stripe starts and ends, without an expensive scan of all the pool’s metadata to find every block pointer.

RAID-Z Expansion is coming to OpenZFS and FreeBSD, made possible by a partnership between the FreeBSD Foundation, iXsystems, and Delphix.