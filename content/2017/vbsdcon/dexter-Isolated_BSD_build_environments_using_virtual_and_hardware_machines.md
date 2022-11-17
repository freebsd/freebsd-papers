---
layout: slides
title: "Isolated BSD build environments using virtual and hardware machines"
date: 2017-09-09
author: Michael Dexter
email: editor@callfortesting.org
youtube: YY_Fkxqy4fg
venue: vBSDCon 2017
---
The rapid pace of BSD development results in a steady flow of new features at the risk of an equally-steady flow of bugs and regressions large and small. Software flaws can, and have remained undetected for decades and been included in formal releases. The difficulty of isolating operating system regressions has traditionally increased proportionately to the age of the software under scrutiny, requiring equally-dated build environments. While the BSDs are exemplary as self-hosting operating systems, this independence is not guaranteed between recent or distant generations of the OSs.

This talk will describe a strategy for using device and PXE-booted virtual machines, plus PXE-booted hardware machines to create isolated build environment that allow for arbitrary source repository revisions to be built under arbitrary OS releases snapshots. While developed with FreeBSD and bhyve with the option of QEMU and jail(8) for extreme regression tracing, this strategy could equally apply to OpenBSD/vmm and NetBSD/Xen.

Michael is a BSD Unix-related author, trainer and support provider who has spoken at BSD conferences since 2008. Michael helped usher the bhyve and Xen hypervisors into FreeBSD and sponsored the SysJail jail mechanism for OpenBSD.
