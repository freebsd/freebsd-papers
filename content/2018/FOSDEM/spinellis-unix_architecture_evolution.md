---
layout: slides
title: "Unix Architecture Evolution from the 1970 PDP-7 to the 2018 FreeBSD"
date: 2018-02-03
author: Diomidis Spinellis
email: dds@aueb.gr
youtube: FbDebSinSQo
---
## Important Milestones and Lessons Learned

Based on a GitHub repository recording the history of the Unix code from 1970 until today, we look at the most significant elements and milestones of the system's architectural evolution and the lessons we can learn from it.

The Unix operating system has had a profound influence on the development of open source software and associated communities. Many of today's systems trace their code or design to a 1970 unnamed operating system kernel, implemented in 2489 lines of PDP-7 assembly language. This evolved into the Unix operating system, whose direct descendants include today's BSD systems and intellectual heirs form the various GNU/Linux distributions.

How did the architecture of Unix evolve over the past half century? Based on a GitHub repository recording the system's history from 1970 until today, a database recording the evolution of provided facilities, and the reconstruction of the Third and Fourth Edition Unix manuals, we will examine the most significant milestones of this development and the lessons we can learn. Many architectural features, such as layering, system calls, devices as files, an interpreter, and process management, were already visible in the 1970 version. Other ideas followed quickly: the tree directory structure, user contributed code, I/O redirection, the shell as a user program, groups, pipes, and scripting. Later versions added domain-specific languages, environment variables, a documented file system hierarchy, software packages, virtual memory support, optimized screen handling, networking, storage pools, dynamic tracing, and a packet capture library. Based on a record of facilities documented over the years we will see areas in which evolution continues at an unchanged pace and areas where it appears stalled. We will also see how one measure of code complexity has followed a self-correcting path. Lessons we can derive from this amazing ride include the durability of early architectural features, the value of establishing conventions over the imposition of rigid mechanisms, the importance of additions made after the system's gestation, and the increasing difficulty of bringing about ground-breaking changes as Unix ages.

## Links

[First Research Edition architecture diagram](https://dspinellis.github.io/unix-architecture/arch-V1.pdf)
[Modern FreeBSD architecture diagram](https://dspinellis.github.io/unix-architecture/arch.pdf)
[Evolution of Unix facilities dataset](https://dspinellis.github.io/unix-history-man/index.html)
[The Unix History Repository](https://github.com/dspinellis/unix-history-repo)
[A visualization of Unix evolution](https://youtu.be/S7JB0mhrGCQ)
[Reconstrution of the Third Edition Manual (nroff)](https://github.com/dspinellis/unix-v3man)
[Reconstrution of the Fourth Edition Manual (troff)](https://github.com/dspinellis/unix-v4man)
