---
layout: paper
title: Kernel-Scheduled Entities for FreeBSD
author: Jason Evans 
email: jasone@freebsd.org
paper: /_assets/other2000_evans_kse.pdf
---
FreeBSD has historically had less than ideal support for multi-threaded application programming. At present, there are two threading libraries available. libc_r is entirely invisible to the kernel, and multiplexes thread sfrom a single process. The linuxthreads port, which creates a separate process for each thread via rfork(), plus one thread to handle thread synchronization, relies on the kernel scheduler to multiplex "threads" onto the available processors.
Both approaches have scaling problems. libc_r does not take advantage of multiple processors and cannot avoid blocking when doing I/O on "fast" devices. The linuxthreads port requires significant kernel resources. In addition, thread switching can only be as fast as the kernel's process switching.
This paper summarizes various methods of implementing threads for applicaition programming, then goes on to describe a new threading architecture for FreeBSD, based on what are called kernel-scheduled entities, or scheduler activations.
