---
layout: slides
title: "LLDB FreeBSD Kernel Module Improvement"
date: 2024-03-25
author: Sheng-Yi Hong
---

This paper introduces the low level debugger (LLDB) kernel module debug facility for the FreeBSD kernel. 
The current functional status of LLDB within the FreeBSD kernel is attributed to contributions from contractor and the collaborative efforts of the community. 
Key functionalities include core dump parsing and memory context building for the coredump, specifically integrated into the process plugin within LLDB for the FreeBSD
kernel. While the implementation of the process plugin has been successfully completed, the paper
emphasizes the imperative need to implement the DynamicLoader plugin for the kernel loader. This plugin plays a critical
role in loading the symbol file of the kernel module, ensuring comprehensive parsing of symbols for loadable kernel modules.

