---
layout: paper
title: A Scalable Concurrent malloc(3) Implementation for FreeBSD
date: 2006-01-01
author: Jason Evans
email: jasone@freebsd.org
slides: /_assets/bsdcan2006_evans_jemalloc_slides.pdf
paper: /_assets/bsdcan2006_evans_jemalloc.pdf
---
The FreeBSD project has been engaged in ongoing work to provide scalable support for multi-processor computer systems since version 5. Sufficient progress has been made that the C library’s malloc(3) memory allocator is now a potential bottleneck for multi-threaded applications running on multiprocessor systems. In this paper, I present a new memory allocator that builds on the state of the art to provide scalable concurrent allocation for applications. Benchmarks indicate that with this allocator, memory allocation for multi-threaded applications scales well as the number of processors increases. At the same time, single-threaded allocation performance is similar to the previous allocator implementation.
