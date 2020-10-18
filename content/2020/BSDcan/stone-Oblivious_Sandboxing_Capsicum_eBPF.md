---
layout: video
title: "Oblivious Sandboxing with Capsicum and EBPF"
date: 2020-06-05
author: Ryan Stone
email: rstone@FreeBSD.org
youtube: TGA4wbjbqXc
---
The Capsicum sandboxing framework currently has the limitation that programs must have their source modified to make them amenable to sandboxing. A long-term goal of the project is oblivious sandboxing: running programs with no knowledge of Capsicum inside of a sandbox with the full protections offered by Capsicum. This would allow the sandboxing of third-party applications that are unlikely to accept large patches for Capsicum support.

In this talk, we build upon previous work in this area to demonstrate how eBPF bytecode programs can be used to realize the promise of oblivious Capsicum sandboxing. By adding an eBPF entry point in the syscall path, it is possible to write eBPF programs that dynamically transform disallowed operations performed by the sandboxed application into operations allowed by Capsicum.

We will begin with an overview of eBPF and its programming environment. We will then show how an eBPF program can intercept a syscall at runtime and change its behaviour. Using this ability, we will demonstrate eBPF programs that force existing applications to conform to the restrictions placed by Capsicum while maintaining their behaviour. Using real-world programs like clang and tar as examples, we will show the eBPF programs and the extensions to the eBPF runtime required to safely sandbox these programs without requiring source modifications.
