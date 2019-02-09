---
layout: paper
title: Problems updating FreeBSD's card system from ISA to PCI
date: 2002-02-13
author: M. Warner Losh
email: imp@freebsd.org
---
FreeBSD's 16-bit PC Card implementation has used the ISA legacy interface. PCI support was added by making PCI-CardBus and PCI-PCMCIA bridges behave in ISA compatibility mode. While this technique worked in laptops, it made support of add-in PCI cards with CardBus or PCMCIA bridges impossible. PCI-PC Card bridges are unlike traditional devices because they can have connections to multiple busses, offering both ISA and PCI interrupt routing for them and any devices connected to them. Expanding support to add-in PCI cards with 16-bit PC Cards connected exposed weaknesses in the PC Card implementation of FreeBSD as well as other parts of the system. Vendor BIOS quality, variance in hardware implementation details from standard and weaknesses in the FreeBSD development model made incorporation of these improvements into FreeBSD 4.4-RELEASE difficult. Lessons learned will be incorporated into the 32-bit CardBus support forthcoming in FreeBSD 5.0. 
