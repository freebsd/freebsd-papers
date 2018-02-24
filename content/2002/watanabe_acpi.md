---
layout: paper
title: ACPI implementation on FreeBSD 
date: 2002-01-01
author: Takanori Watanabe
email: 
paper: /_assets/other2002_watanabe_acpi.pdf
---
Prior to the introduction of the Advanced Configuration and Power Management Interface (ACPI), PCs did not have a unified standard mechanism that allowed the operating system to enumerate, configure, and manage the power usage and thermal properties of builtin hardware devices. Instead, these devices were either left unmanaged, or they were managed by special BIOS-level code such as Plug-and-Play BIOS (PnP BIOS), Advanced  Power  Management  BIOS  (APM), or other vendor-specific BIOS code. These firmware-driven methods increase firmware costs, and the resulting BIOS code is difficult to alter or debug. Device management issues are  becoming more important,  especially in moble computing environments where finegrain power management is often necessary. ACPI replaces PnP BIOS, APM, and a number of ad hoc methods while providing a management framework that allows increased flexibility in hardware design. Unfortunately, the increased power and flexibility of ACPI comes with a cost: it requires substantial software support from the operating system kernel. In this paper we describe ACPI, how it is implemented in FreeBSD, and the lessons we learned from working with ACPI.
