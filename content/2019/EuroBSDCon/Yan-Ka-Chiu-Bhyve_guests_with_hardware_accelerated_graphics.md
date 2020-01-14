---
layout: slides
title: "Bhyve guests with hardware accelerated graphics"
date: 2019-09-21
author: Yan Ka Chiu
youtube: ckqveGsIcA0
---
FreeBSD is not only a great platform for server, it is also a brilliant choice for workstation and desktop. However, there’re still a lot of applications that are not *BSD aware. The solution is Bhyve, the BSD Hypervisor which allows you to run these applications in virtual machines on top of FreeBSD. You also want these fancy, graphically intensive desktop applications to run smooth! Therefore a Smart BSD user like you automatically think about GPU passthrough…. and you quickly realise it’s not support as listed in the bhyve Wiki.

*Or is it? *

If you are someone like me who run FreeBSD-CURRENT on your primary workstation, you may have encountered the following problems:

 * Your new shinny RTX graphics card won’t work in CURRENT because the official Nvidia driver only support up to 12-STABLE and the driver from ports only support up to 1080Ti.
 * You need to run some applications in a Bhyve Virtual machines that’s graphically intensive
 * You want to accelerate OpenGL on *nix VM.

This talk will introduce you some tricks to enable usable GPU passthrough and other tricks to enable hardware acceleration for bhyve guests.
