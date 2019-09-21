---
layout: handout
title: GEOM tutorial
date: 2003-09-11
author: Poul-Henning Kamp
email: phk@FreeBSD.org
---
GEOM is the new disk I/O subsystem in FreeBSD 5.x. It provides an
extensible and modular framework for "doing things" to disk I/O
requests. It allows you to recognize Apple partitions on your PC
and Solaris partitions on your Alpha, mirror your striped disks,
stripe your mirrored disks, and even stripe your encrypted, mirrored
Apple partitions on your Sparc64 computer.
