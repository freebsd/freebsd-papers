---
layout: paper
title: "Institutionalizing FreeBSD Isolated and Virtualized Hosts Using bsdinstall(8), zfs(8) and nfsd(8): Authentic jail and VM hosts are best created with authentic tools"
date: 2018-06-08
author: Michael Dexter
youtube: C8gei7BadqI
paper: dexter-Institutionalizing_FreeBSD_Isolated_and_Virtualized_Hosts-paper.pdf
---
The FreeBSD installer bsdinstall can be easily modified to create block and file-backed "guest" hosts for jail, bhyve and Xen, but with the addition of ZFS, NFS and DHCPd, a highly flexible environment can be built that both supports booting FreeBSD as far back as 5.0 and booting boot environments on both virtual machines and real hardware machines on the network. These abilities are not only useful for decoupling hardware and software machines, but also tracking regressions down to the guilty commits that produced them.

The FreeBSD operating system includes the isolation and virtualization features chroot(8), jail(8), bhyve(8) and Xen, but offers limited abilities for creating and managing jail, bhyve or Xen "guest" hosts. The bsdinstall(8) jail, jail.conf(8), and vmrun.sh tools support rudimentary jail and bhyve guest host creation and management but are not designed for automation using in-base or external tools. This talk will describe how the bsdinstall(8), nfsd(8) and zfs(8) in-base resources can be leveraged to create authentic, file and block storage-backed FreeBSD root installations suitable for use with not only jail(8), bhyve(8) and Xen, but also network-booted hardware machines. Leveraging in-base tools in support of in-base isolation and virtualization features not only makes it easer to create guest hosts, but also enables the comprehensive testing of current and past versions FreeBSD in pursuit of regressions.

Of the leveraged components:

* bsdinstall is extended (work completed and under peer review) to remove assumptions of a "fresh install" and to support "nested" or "deep" boot environments as supported by /etc/rc.d/zfsbe.
* ZFS is used to both to provide zvols for block-backed virtual machines and boot environments for jail and NFS-shared bhyve virtual machines.
* The in-kernel NFSd is used to provide high-performance "root on NFS" support for software and hardware machines.

The methodologies described in this talk should apply in part or in full to other BSD operating systems.