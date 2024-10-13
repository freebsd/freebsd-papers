---
layout: paper
title: "Why fsync() on OpenZFS can’t fail (and what happens when it does)"
date: 2024-03-23
author: Rob Norris
email: robn@despairlabs.com
venue: AsiaBSDCon 2024
---

On OpenZFS, fsync() cannot fail - it will wait until the application’s changes
are on disk before it returns. If there is a problem, such as a hardware
failure, that causes the pool to suspend, then it may wait forever. This feels
strange, but is acceptable according to the API contract: fsync() never
returned success, so the application has no reason to believe its data is on
disk.

However, OpenZFS pools can recover if the fault is repaired, and so fsync() can
still return. As it turns out though, it’s possible in rare situations for the
pool to return to service but not have actually put the data on disk. fsync()
returns success, because it cannot fail, and the application has been lied to.

This paper describes the path taken from the fsync() call, through the ZFS
Intent Log, the transaction machinery, the pool failure system and the IO
pipeline to understand what happens to IO when disks fail, and why OpenZFS
believed that writes had succeeded when they had not. It goes on to describe
changes to make OpenZFS understand that something had gone wrong and respond
appropriately, such that fsync() once again cannot fail.
