---
layout: slides
title: "How ZFS snapshots really work and why they perform well (usually)"
date: 2019-05-17
author: Matt Ahrens
email:  matthew.ahrens@delphix.com
youtube: NXg86uBDSqI
---
Snapshots are one of the defining features of ZFS. They are also the foundation of other advanced features, such as clones and replication with zfs send / receive. If you have ever wondered how much space your snapshots are using, you’ll want to come to this talk so that you can understand what “used” really means! If you want to know how snapshots can be so fast (or why they are sometimes so slow), this talk is for you! I designed and implemented ZFS snapshots, starting in 2001. Come to this talk and learn from my mistakes!

In this talk I will explain:

* How ZFS snapshots are implemented, why the data structures and algorithms were chosen, and how they impact performance - especially of snapshot deletion, which is the most performance-critical snapshot operation.
* Snapshot space accounting - the difference between the “used”, “referenced”, and “written@...” properties, which one you should be looking at, and how they are implemented.
* How the implementation has changed over time to better scale when there are a large number of snapshots.
* Proposals for future work to further improve performance.