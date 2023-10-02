---
layout: slides
title: "ZFS Directory Scaling"
date: 2023-09-17
author: Mateusz Piotrowski
youtube: RFy6VtDwQ8U
---
It is not uncommon to store thousands of files in a single directory.
Unfortunately, a growing directory size may result in unexpected bottlenecks
slowing down the system. The performance hit can be observed even for simple
operations like lookup, open, and create.

What are the data structures defining the performance of directories? What
obscure tunables are worth taking a look at when storing thousands of files in
thousands of directories? What are the recent developments in OpenZFS helping
to address those performance problems?

The presentation walks the audience through the realm of OpenZFS performance
engineering. First, it introduces the audience to the essential concepts in ZFS
and provides the 101 of file system performance tuning. Afterwards, it takes a
deep dive into the implementation of directories in OpenZFS. Finally, the
presentation presents ways of improving ZFS directory scaling, discusses
relevant tunables and how to use them, and comments on the in-progress work and
recent developments in OpenZFS.
