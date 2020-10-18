---
layout: video
title: "Thunderbolt on FreeBSD"
date: 2020-06-05
author: Scott Long
youtube: VbAJf2PBE-M
---
Thunderbolt3 combines external USB3, PCIe, and DisplayPort peripherals into a converged interface. While the original intent was that OS-specific drivers would not be needed for peripherals to function, the reality is that a driver is needed to interact with the security features of the subsystem, flash firmware, and manage bandwidth and error handling. Additionally, the OS must provide robust PCI hotplug support in order to handle device arrival and departure.

This talk will present the architecture of the FreeBSD thunderbolt driver, the challenges faced with hot-plug, and the roadmap for future support, including USB4.
