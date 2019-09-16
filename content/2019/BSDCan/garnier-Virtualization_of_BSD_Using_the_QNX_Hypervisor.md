---
layout: slides
title: "Virtualization of BSD Using the QNX Hypervisor"
date: 2019-05-17
author: Quentin Garnier
email: qgarnier@blackberry.com
---
Getting a BSD running on a new virtualization platform raises challenges both on the guest and the host sides. Hypervisors present weird hardware to their guests that looks like actual hardware to a great extent with some unexpected twists.

The talk will explore the process of porting NetBSD and FreeBSD (x86 and ARMv8) to the QNX Hypervisor (or is it the other way around?).

Virtualization of guest operating systems by way of a hypervisor is not new. BSD has been guested on Windows/Linux for many years.

What is new is the movement to guest mainstream operating systems inside embedded systems. The benefits for embedded device development and runtime are many: isolation of functional safety from non-safety code, security/isolation, re-use of code, faster development. Couple this with standards such as VirtIO that are pre-integrated into the guest and you have a ready to go solution.

This seminar will discuss the technical issues in guesting BSD by way of an embedded hypervisor. The embedded hypervisor used for discussion will be the QNX microkernel-based hypervisor. However the concepts are the same for all embedded hypervisors that use a trap/emulate/virtualize/return model of hardware virtualization. Both ARMv8 (AArch64) and Intel x86_64 with VT-x systems will be discussed; with an emphasis on the hardware/software support required and configuration needed for BSD to enable it to run on a typical embedded hypervisor.