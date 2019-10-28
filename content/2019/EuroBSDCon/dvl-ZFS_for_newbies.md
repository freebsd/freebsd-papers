---
layout: slides
title: "ZFS for newbies"
date: 2019-09-22
author: Dan Langille
email: dvl@freebsd.org
---
Dan Langille thinks ZFS is the best thing to happen to filesystems since he stopped using floppy disks. ZFS can simplify so many things and lets you do things you could not do before. If you’re not using ZFS already, this entry-level talk will introduce you to the basics. Things we will cover include:

 * a short history of the origins
 * an overview of how ZFS works
 * replacing a failed drive
 * why you don’t want a RAID card
 * scalability
 * data integrity (detection of file corruption)
 * why you’ll love snapshots
 * sending of filesystems to remote servers
 * creating a mirror
 * how to create a ZFS array with multiple drives which can lose up to 3 drives without loss of data.
 * mounting datasets anywhere in other datasets
 * using zfs to save your current install before upgrading it
 * simple recommendations for ZFS arrays
 * why single drive ZFS is better than no ZFS
 * no, you don’t need ECC
 * quotas
 * monitoring ZFS
