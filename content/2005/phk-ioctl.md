---
layout: slides
title: Ioctl(2) is so 1980ies
date: 2005-05-14
author: Poul-Henning Kamp
email: phk@FreeBSD.org
---
Proper design of userland kernel APIs is changing with the times.
Once ioctl() was the catch-all way to communicate things, but that
was back when both software and hardware stayed the same from boot
to crash. With loadable modules and pluggable hardware, ioctl() is
just not enough.

Poul-Henning will talk about the concerns to be addressed and methods
available to design modern APIs, and go through a number of his
creatations: GEOMs XML export and g_ctl(). nmount(2). device_statistics
export etc.
