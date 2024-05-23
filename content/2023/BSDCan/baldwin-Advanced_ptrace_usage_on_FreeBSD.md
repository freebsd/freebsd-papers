---
layout: slides
title: "Advanced ptrace() usage on FreeBSD"
date: 2023-05-19
author: John Baldwin
email: jhb@FreeBSD.org
youtube: QDjkj-URxrM
venue: BSDCan 2023
---

Over the past year I have worked on several changes to the FreeBSD
native target in the GDB debugger to support debugging of multiple
concurrent processes. This talk will cover how this is implemented
using ptrace(). It will also discuss potential changes to ptrace() to
reduce the number of system calls required for common cases as well as
potential changes needed in the future to support non-stop debugging.
