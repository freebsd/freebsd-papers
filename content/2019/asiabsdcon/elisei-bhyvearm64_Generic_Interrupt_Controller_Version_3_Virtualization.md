---
layout: paper
title: "bhyvearm64: Generic Interrupt Controller Version 3 Virtualization"
date: 2019-03-23
author: Alexandru Elisei, Mihai Carabas
email: alexandru.elisei@gmail.com, mihai.carabas@upb.ro
paper: elisei-bhyvearm64_Generic_Interrupt_Controller_Version_3_Virtualization.pdf
---
Traditionally associated with low-power, mobile computing, Arm is now seeking to enter the PC and the server markets. Virtualization is especially used in these areas, and current hypervisors rely on various hardware features to achieve efficient virtualization. To this end, the Armv8 architecture introduces a series of hardware mechanisms to reduce or eliminate some of the overhead associated with running virtual machines. Modern computers rely on hardware interrupts to communicate with peripherals, and this aspect of virtualization has seen a series of architectural optimizations from Arm. We will present our experience emulating the Generic Interrupt Controller version 3, the interrupt controller designed by Arm. We have used a mix of virtualization techniques: trap-and-emulate for the memory-mapped regions of the controller, which are accessed less frequently, and hardware accelerated virtualization where possible. To validate our approach, we have created a virtualized timer which is used to deliver timer interrupts to the virtual machines. Timers are essential for modern operating systems, and the virtualized timer is an abstraction over the Arm architectural timer, the Generic Timer. As with the interrupt controller, we have taken special care to take advantage of the available hardware mechanisms to reduce the cost of virtualization. The end result is a fully functioning hypervisor which is able to create, run and destroy virtual machines on Armv8.0-A and later processors.
