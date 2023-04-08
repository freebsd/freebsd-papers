---
layout: slides
title: "smart(8) Update: A Permissively-Licensed Alternative to smartctl(8)"
date: 2021-09-19
author: [ "Michael Dexter", "Chuck Tuffli" ]
email: [ "editor@callfortesting.org", "chuck@tuffli.net" ]
youtube: 4HHZOEp8KrE
venue: EuroBSDCon 2021
---

The familiar smartctl(8) utility from the SmartMonTools package has helped
operators access the S.M.A.R.T. storage device health diagnostics since its
introduction in 199*. While smartctl(8) is proven, flexible, and widly-ported,
it has long been limited in the machine-readability of its output, burdened by
support for long-discontinued devices, and published under a license that
precludes its inclusion in permissively-licensed operating systems such as a
FreeBSD, NetBSD, and OpenBSD. The smart(8) utility conceived of by Michael
Dexter and authored by Chuck Tuffli addresses many shortcomings of smartctl(8)
by focusing on machine-readability, contemporary storage devices, and
publication under a BSD two-clause license. This talk will provide a history
of diskctl(8) come smart(8) and its motivations, an overview of its
implementation and porting to additional platforms including Microsoft
Windows, and a tour of its latest features including TSV, libxo, and JSON
output.

**Michael Dexter**

Michael has used Unix systems since just prior to the announcement of the
Linux kernel and collapse of the Soviet Union. He has helped raise money for
various BSD development efforts and usher the bhyve hypervisor into the
FreeBSD operating system. Michael lives in Portland, Oregon where he provides
commercial OpenZFS and FreeNAS support, hosts the Portland Linux/Unix Group,
and lives with his wife and three children.

**Chuck Tuffli**

Chuck is a FreeBSD committer and has primarily worked as an OS/device driver
developer on Unix-like operating systems for a variety of technologies
including video, graphics, wireless and storage devices. He has written
several FreeBSD CAM device drivers and contributed to the CAM Target Layer
(ctl), Linuxulator, NVMe driver and NVMe emulator.
