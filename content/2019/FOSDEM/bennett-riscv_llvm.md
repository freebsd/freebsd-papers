---
layout: slides
title: "Embedded FreeBSD on a five-core RISC-V processor using LLVM"
date: 2019-02-02
author: Jeremy Bennett
youtube: c6_g5KMUX-E
---
In this talk we describe our experience of bringing up embedded FreeBSD for a heterogeneous 32/64-bit RISC-V system using LLVM, which was more difficult than you might expect. We look at the practical engineering steps needed to bring up an embedded operating system where many of the key components are not fully mature. The result is a reference embedded FreeBSD implementation for RISC-V, freely available to the community.

We were tasked with bringing up and testing embedded FreeBSD on a custom five-core 32/64-bit RISC-V processor using LLVM. Given FreeBSD has already been ported to RISC-V and LLVM is the standard BSD C/C++ compiler surely this should be easy.

But it wasn't. LLVM for RISC-V is still relatively immature, particularly for 64-bit. FreeBSD runs on symmetric multi-core 64-bit QEMU RISC-V, but not on embedded systems and not on heterogeneous multicore systems.

In this talk we'll go through the steps needed to bring up a functioning embedded FreeBSD system on multi-core heterogeneous RISC-V system. Our target hardware was not available at the start of the project, so we used the generally available HiFive Freedom Unleashed board. The result is a reference embedded FreeBSD implementation for RISC-V, freely available to the community.

This is not a talk about the deep internals of FreeBSD, but about the practical engineering steps needed to bring up an embedded operating system where many of the key components are not yet fully mature.
