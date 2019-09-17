---
layout: video
title: "Adventure in DRMland: Or how to write a drm driver for an arm64 SoC"
date: 2019-05-17
author: Emmanuel Vadot
email: manu@freebsd.org
youtube: axucgdUziYQ
---
In this talk I will describe the needed steps to write a DRM (As in Direct Rendering Manager) driver on FreeBSD for an arm64 board.

DRM is the defacto standard to have graphics on a modern system using the standard software stack like Xorg or Wayland.

While FreeBSD amd64 have correct support for DRM drivers, arm and arm64 are way behind and except on some system like Raspberry Pi where a simple framebuffer is available or NVidia Tegra where a DRM driver is available, the only way to have graphics is to use EFIFB. Both EFIFB and the simple framebuffer on RPI have severe limitations. You cannot have 2D acceleration, have a multi screen setup or even change the resolution at runtime.

Writing a DRM driver can be hard and scary, especially when it is the first one that you are writing and don't know the DRM subsystem API.

During this talk I'll explain what a DRM driver is consisted of : framebuffer, planes, crtc and encoder won't have anymore secrets for you.

You will see why I've chosen to write my first DRM driver for the Allwinner A64 (An ARM64 System on Chip present on the Pine64 board or on the Pinebook, a cheap laptop), what problems I had and how I solved them. Of course a driver related talk will not be complete without a tips and tricks part that will help you having graphics shown on your screen quicker.