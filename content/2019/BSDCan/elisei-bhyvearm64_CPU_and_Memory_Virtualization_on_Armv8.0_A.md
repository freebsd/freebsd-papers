---
layout: slides
title: "bhyvearm64: CPU and Memory Virtualization on Armv8.0-A"
date: 2019-05-18
author: Alexandru Elisei
email: alexandru.elisei@gmail.com
youtube: rh3-62HHkYY
---
bhyve is FreeBSD’s hypervisor, and we have been working on porting it to the Armv8.0 architecture, port which we have called bhyvearm64. We will present the current status of the project, the architecture of the hypervisor, as well as how we have used the hardware features which were designed for virtualization. To provide the guest with an abstracted view of the processor we have used a third CPU execution mode, Exception Level 2. To restrict the guest to a memory region of our choosing we have used an extra address translation step called Stage 2 Translation.

Virtualization allows a host computer to run multiple virtual machines. The Armv8 family of processors provides various hardware features which make virtualization efficient by removing or reducing some of the overhead usually associated with running virtual machines. bhyve is FreeBSD’s hypervisor and has been originally created to implement virtualization on the x86 platform. We have been working on porting bhyve to the Armv8.0 architecture, port which we have called bhyvearm64.

We will present the current status of the hypervisor: about what features are implemented, what we have used for testing and what the current limitations are. bhyvearm64 follows the same architecture as bhyve, which uses three user space programs to create, run and terminate a virtual machine: bhyveload, bhyve and bhyvectl, respectively. The hypervisor itself is implemented as a kernel module named vmm which can be loaded at runtime.

All Armv8 CPUs have two different execution modes, called Exception Levels, to separate non-privileged user processes from the kernel. To aid virtualization, a third Exception Level, Exception Level 2, has been added as an optional hardware extension and this execution mode provides the needed separation between a guest and the host operating system.

A hypervisor needs to have control over the memory locations that a guest virtual machine is able to access. Historically, this has been done by emulating the page tables in software, which can incur a significant hardware penalty. To reduce this overhead, ARM has implemented a second stage of address translation, called stage 2 translation, as part of the virtualization extensions. We use this feature to isolate a region of memory which will be made available to the virtual machine.
