---
layout: video
title: "Asynchronous and Direct I/O for PostgreSQL on FreeBSD"
date: 2022-06-03
author: Thomas Munro
youtube: 5znybwzUZog
---
I've been working on parts of a next generation I/O subsystem that will be proposed for PostgreSQL 16. I will give a report on the motivation, results so far, things learned along the way while implementing the FreeBSD/POSIX AIO support (and others), and some ideas on how to improve FreeBSD. Topics will include:

- a quick tour of PostgreSQL/AIO on FreeBSD, and how to try it out
- why are database hackers obsessed with direct I/O?
- why do direct I/O and async I/O go together?
- DIO APIs and implementations (anticipated ZFS support, existing UFS support, others)
- AIO APIs and implementations (venting about POSIX, comparing to other systems)
- kqueue is wonderful -- how can we get more kqueue?
- stumbling blocks
- thing I'd love to improve in FreeBSD I/O
- me learning where I'm wrong from I/O stack experts
