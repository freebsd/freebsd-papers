---
layout: slides
title: "Multiple Passes of the FreeBSD Device Tree"
date: 2009-05-09
author: John Baldwin
email: jhb@FreeBSD.org
paper: article.pdf
venue: BSDCan 2009
---
The existing device driver framework in FreeBSD works fairly well for many
tasks.  However, there are a few problems that are not easily solved with the
current design.  These problems include having "real" device drivers for
low-level hardware such as clocks and interrupt controllers, proper resource
discovery and management, and allowing most drivers to always probe and attach
in an environment where interrupts are enabled.  I propose extending the device
driver framework to support multiple passes over the device tree during boot.
This would allow certain classes of drivers to be attached earlier and perform
boot-time setup before other drivers are probed and attached.  This in turn can
be used to develop solutions to the earlier list of problems.
