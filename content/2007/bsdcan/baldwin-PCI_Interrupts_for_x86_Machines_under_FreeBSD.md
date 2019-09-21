---
layout: slides
title: "PCI Interrupts for x86 Machines under FreeBSD"
date: 2007-05-18
author: John Baldwin
email: jhb@FreeBSD.org
paper: article.pdf
venue: BSDCan 2007
---
An important element in computers with multiple autonomous devices is
the ability of a device to notify the CPU that it needs attention via
an interrupt.  The OS visible mechanics of interrupts for PCI devices
is quite convoluted, especially on x86 PC systems.  This paper will
cover the various ways that PCI INTx interrupts have been implemented
on x86 as well as the methods used by the system BIOS to communicate
the implementation to operating systems.  It will also cover the newer
Message Signalled Interrupts that address some of the limitations of
INTx interrupts.  Finally, the paper will provide an overview of
FreeBSD's implementation of both INTx and MSI interrupts on the x86
platform.
