---
layout: video
title: "Fuzzing the kernel"
date: 2019-09-21
author: Andrew Turner
email: andrew@freebsd.org
youtube: yyQFdWJDmh0
---
Modern C compilers include support for tools to help find bugs in code. These
tools, the sanitizers, add instrumentation to the generated code that can be
compiled into the kernel to help the kernel developers. In early 2018 I became
interested in using these in the FreeBSD kernel to assist bug finding and
debugging.

This talk will discuss the current state of kernel sanitizers on FreeBSD. This
will include the kernel coverage sanitizer that can be used with fuzzers, the
undefined behaviour sanitizer to warn when code relies on undefined behaviour,
and the address sanitizer to detect out of bounds accesses. It will also discuss
future work to port new sanitizers and the use hardware based acceleration.

The main fuzzer to use these sanitizers is the syzkaller fuzzer from Google. I
will talk about my experiences using this, bugs it has found, and future work to
port other fuzzers to work with the kernel.

**Andrew Turner**

Andrew is a FreeBSD committer known for porting FreeBSD to the 64 bit Arm
architecture. Recently he has worked on improving the kernel code quality by
enabling kernel fuzzing through compiler sanitizers.

Andrew works as a Freelance Software Engineer and a Research Associate at the
University of Cambridge working on the CHERI project. He is interested in using
existing and novel hardware features to help improve code quality and security.
