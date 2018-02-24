---
layout: paper
title: Malloc(3) revisited
date: 1998-01-01
author: Poul-Henning Kamp
email: phk@freebsd.org 
paper: /_assets/usenix1998_kamp_malloc.pdf
---
malloc (3) is one of the oldest parts of the C language environment and not surprisingly the world has changed a bit since it was first conceived. The fact that most UNIX kernels have changed from swap/segment to virtual memory/page based memory management has not been sufficiently reflected in the implementations of the malloc/free API.
A new implementation was designed, written, tested and bench-marked with an eye on the workings and performance characteristics of modern Virtual Memory systems. It works OK.
