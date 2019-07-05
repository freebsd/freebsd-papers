---
layout: slides
title: "Fuzzing the kernel: Porting the Clang Sanitizers to FreeBSD"
date: 2019-05-17
author: Andrew Turner
email: andrew@FreeBSD.org
youtube: 1tYtT8Jk21c
---
Modern C compilers include support for tools to help find bugs in code. These tools, the sanitizers, add instrumentation to the generated code that can be compiled into the kernel to help the kernel developers. In early 2018 I became interested in using these in the FreeBSD kernel to assist bug finding and debugging.

This talk will discuss the current state of kernel sanitizers on FreeBSD. This will include the kernel coverage sanitizer that can be used with fuzzers, the undefined behaviour sanitizer to warn when code relies on undefined behaviour, and the address sanitizer to detect out of bounds accesses. It will also discuss future work to port new sanitizers and the use hardware based acceleration.

The main fuzzer to use these sanitizers is the syzkaller fuzzer from Google. I will talk about my experiences using this, bugs it has found, and future work to port other fuzzers to work with the kernel.
