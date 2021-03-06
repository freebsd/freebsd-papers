---
layout: slides
title: "KLEAK - Practical Kernel Memory Disclosure Detection"
date: 2019-02-02
author: Thomas Barabosch
email: thomas.barabosch@fkie.fraunhofer.de 
youtube: 56YbLjw0nds
---
Kernel memory disclosures - also known as kernel information leaks - denote the inadvertent copying of uninitialized bytes from kernel space to user space. Such disclosed memory may contain cryptographic keys, information about the kernel memory layout, or other forms of secret data. Even though kernel memory disclosures do not allow direct exploitation of a system, they lay the ground for it.

We introduce KLEAK, a simple approach to dynamically detect kernel information leaks. Simply said, KLEAK utilizes a rudimentary form of taint tracking: it taints kernel memory with marker values, lets the data travel through the kernel and scans the buffers exchanged between the kernel and the user space for these marker values. By using compiler instrumentation and rotating the markers at regular intervals, KLEAK significantly reduces the number of false positives, and is able to yield relevant results with little effort.

Our approach is practically feasible as we prove with an implementation for the NetBSD kernel. A small performance penalty is introduced, but the system remains usable. In addition to implementing KLEAK in the NetBSD kernel, we applied our approach to FreeBSD 11.2. In total, we detected 21 previously unknown kernel memory disclosures in NetBSD-current and FreeBSD 11.2, which were fixed subsequently. As a follow-up, the projects’ developers manually audited related kernel areas and identified dozens of other kernel memory disclosures.

