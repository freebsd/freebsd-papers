---
layout: slides
title: "FreeBSD and GDB"
date: 2016-06-11
author: John Baldwin
email: jhb@FreeBSD.org
youtube: XVkOmFCQr9o
venue: BSDCan 2016
---
This talk will focus on FreeBSD-specific details of the gdb debugger
in the devel/gdb port.

In the past year, several changes have been added to devel/gdb (many
of them upstreamed) including support for fork following and a new
thread target.  In addition, the kgdb kernel debugger has been ported
to GDB 7.x including support for cross-debugging crashdumps.  The talk
will cover both the use of these recent changes as well as how they
were implemented.
