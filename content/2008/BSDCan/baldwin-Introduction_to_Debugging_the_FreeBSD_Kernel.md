---
layout: slides
title: "Introduction to Debugging the FreeBSD Kernel"
date: 2008-05-17
author: John Baldwin
email: jhb@FreeBSD.org
paper: article.pdf
venue: BSDCan 2008
---
Just like every other piece of software, the FreeBSD kernel has bugs.
Debugging a kernel is a bit different from debugging a userland
program as there is nothing underneath the kernel to provide debugging
facilities such as ptrace() or procfs.  This paper will give a brief
overview of some of the tools available for investigating bugs in the
FreeBSD kernel.  It will cover the in-kernel debugger DDB, the kernel
tracing facility KTR, and using kgdb to perform post-mortem analysis
on kernel crash dumps.
