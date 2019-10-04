---
layout: slides
title: "Heart ticking for a guest running on FreeBSD ARM hypervisor"
date: 2019-05-18
author: Mihai Carabas
email: mihai@freebsd.org
youtube: OGMBwnx6J-Y
venue: BSDCan 2019
---
Interrupts are used in modern systems to signal events that require immediate action. Current CPUs implement interrupts using some type of controller circuit. As such, the ARM architecture uses a system called Generic Interrupt Controller to manage interrupts. In order for virtualization to be possible on ARM hardware, a Virtual Generic Interrupt Controller needs to be present to manage interrupts for guest operating systems. This research project describes implementing such a system for an ARMv7 processor running the FreeBSD hypervisor - bhyve. Also to have a fully reponsive guest, we present the timer virtualization implementation.

In the past, handling of external events - such as keyboard input - was done by polling the respective device in order to check whether any processing was required. This method was inefficient due to the difficulty of balancing the promptness of responding to an event versus the time spent in polling. Furthermore, the method did not scale well with the number of sources of possible events.

The alternative developed in order to overcome these shortcomings consists of using an interrupt system. In such a system, an interrupt controller is connected to both the CPU and any devices that may generate events that require handling by the operating system. Whenever such an event occurs, the interrupt controller signals the CPU that an interrupt has occurred and sends a number which identifies the interrupt. In response, the processor saves the current execution state and jumps to the interrupt handler associated to the identifier it has received.

Actual implementation details depend on hardware. However, all platforms use some type of interrupt controller in order to manage interrupts. Intel processors use an interrupt controller known as Advanced Programmable Interrupt Controller (APIC). ARM uses a different system, called Generic Interrupt Controller, which is further discussed in this paper.

Timed events are a core element of many software systems. Their utility ranges from pre-empting processes while in kernel space to scheduling events in high level programming in user space. It is clear that these types of functionality are also desirable when running software in a virtualized environment.

The need for keeping time has brought about the introduction of new timer hardware, such as the Programmable Interval Timer(PIT), the Real Time Clock(RTC), the Advanced Configuration and Power Interface(ACPI) and the High Precision Event Timer(HPET), each with their own utility.

[Bhyve ARM repo](https://github.com/FreeBSD-UPB/freebsd/tree/projects/bhyvearm)