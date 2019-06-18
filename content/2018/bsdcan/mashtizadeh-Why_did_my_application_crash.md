---
layout: paper
title: "Why did my application crash? Practical Low Overhead Record/Replay in FreeBSD"
date: 2018-06-09
author: Ali Mashtizadeh
email: mashti@uwaterloo.ca
youtube: dxpzis2riZc
paper: asplos17-castor-Towards_Practical_Default-On_Multi-Core_Record_Replay.pdf
---
Diagnosing crashes from core dumps is painful and time consuming. Record/replay offers an alternative, allowing buggy program execution to be recorded and reproduced when crashes occur.

Tools that use record/replay to capture live bugs, or to provide an enhanced debugging experience are becoming increasingly common, including commercial offerings for Linux by UndoDB and RogueWave, Mozilla’s rr, and recently added support for replay in WinDBG.

We describe our ongoing work to build a practical record/replay system for FreeBSD called Castor. Castor offers several novel capabilities compared to other record/replay systems, most notably the ability to record demanding multi-core workloads with very low overhead, making it practical to use in production settings.

This talk will explore the basics of record and replay and its applications, then dive into Castor's internals and performance. We will do a live demonstration of how to use Castor to capture and diagnose application bugs. We will talk about how Castor integrates with FreeBSD including Clang/LLVM support, and changes to libc to support cleaner system call interposition for Castor and similar tools with the addition of libsyscall. We will talk about ongoing work to make record/replay logging more space efficient through incremental checkpointing, and potential future applications of record/replay such as efficient fault tolerance.

By the time of this talk Castor will be available in ports, and patches to support Castor will be enabled on BSD head.

The academic paper below details the design and implementation of an earlier version of Castor and was given at ASPLOS 2017.