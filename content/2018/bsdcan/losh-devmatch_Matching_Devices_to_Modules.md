---
layout: slides
title: "devmatch -- matching devices to modules: PNP plays matchmaker for kernel modules"
date: 2018-06-08
author: Warner Losh
youtube: XgnUWG5mAAQ
paper: losh-devmatch_Matching_Devices_to_Modules.pdf
---
FreeBSD ships a large (28MB) kernel by default. One reason is that FreeBSD cannot dynamically load drivers based on their identifying information. All FreeBSD drivers must match this information, and almost all have tables of device ids and other information they use to claim devices. There has been no general way to load these drivers, until devmatch. devmatch uses these tables in kernel modules to match them to devices in the system without drivers. devmatch matches both at boot, and as devices are dynamically added to the system. The kernel is smaller for everybody, while still preserving the convenience of today's larger kernel by loading seldom used drivers as needed.

FreeBSD's kernel has been growing since the earliest days. FreeBSD 1.0R had a kernel that would fit on a floppy drive (the kernel + boot loader fit on a 1.2MB floppy). Now it is approaching 28MB on amd64. A large part of this growth has been due to the drivers. A kernel with all the drivers removed is only about 5MB, meaning over 80% of the kernel is drivers, most of them for devices that aren't in any given system.

Since FreeBSD 3.2, newbus has published information about devices in the system. Each bus has it's own names for the identifying information the devices have, but FreeBSD uses pnpinfo as a generic term for this information. devd was added in FreeBSD 5.0 to generically do things with this information, including when no currently-loaded driver matched a device some self-enumerating bus found. At the time, it was thought it would be a simple matter to generate devd scripts from the plug and play information in the kernel. PC Card and USB drivers all used the the same format in FreeBSD 4, but all other busses were ad-hoc. In FreeBSD 8, USB moved its plug and play information into its own ELF section and extracted by a script to create devd scripts for autoloading.

The experience with USB lead to the next generation design. Starting in FreeBSD 10, kldxref could extract the marked tables embedded in modules, along with metadata describing the table's layour (to better cope with the PCI mess). All the USB and PC Card drivers were marked in FreeBSD 11, as well as a few other drivers with other bus attachments to prove the design. devmatch, to be in FreeBSD 12, looks at the loader.hints file created by kldxref and matches it against unattached devices in the tree. Scripts in /etc/rc.d and devd tie this together.

FreeBSD 12 is anticipated to ship with a smaller GENERIC kernel, with the bulk of the drivers loaded automatically through these means.

devd Paper at 2003 BSD Conference: https://dl.acm.org/citation.cfm?id=1250974
Regenerated graph of FreeBSD commits: https://people.freebsd.org/~imp/freebsd-cumulative.png
Kernel sizes back to the dawn of Unix: https://docs.google.com/spreadsheets/d/13C77pmJFw4ZBmGJuNarBUvWBxBKWXG-jtvARxJDHiXs/edit#gid=0