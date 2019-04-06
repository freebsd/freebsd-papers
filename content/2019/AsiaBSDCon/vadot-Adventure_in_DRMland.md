---
layout: paper
title: "Adventure in DRMland - Or how to write a FreeBSD ARM64 DRM driver"
date: 2019-03-23
author: Emmanuel Vadot
email: manu@freebsd.org
paper: pdf-filename
---
## Adventure in DRMland - Or how to write a FreeBSD ARM64 DRM driver

DRM (Direct Rendering Manager) is today standard for applications like a display server, to talk the the graphical hardware present on a computer or System On a Chip (SoC). It consist of a kernel side API and a userland part (via IOCTLs) that application can use to talk the GPU or configure the display modes (resolution, refresh rates etc ...). While support for X86 devices (intel or amd) are now correct on FreeBSD, arm and arm64 hardware support is still lacking. The only DRM driver is for Tegra based SoC, other hardware either have basic framebuffer support (like the RaspberryPi family) or will require the bootloader to have framebuffer support and will use it via EFI Graphic OutPut Protocol. While framebuffer might be enough for some use, having a DRM driver brings a lots of possibility, 2D acceleration, changing resolution, hotpluging another monitor etc ? And it is also mandatory if we want to support the 3D chip or the Video decoder usualy present on arm/arm64 SoCs. In this paper the author will describe the DRM subsystem and the anatomy of a modern DRM driver, based on his work on the Allwinner Display Engine 2 present in many SoC of this semiconductor company.
Note: you can exclude any frontmatter you do not need (youtube, video, paper, etc)

Layouts:
slides (standard, links to all files and small embed of video)
paper (large embed of the PDF referred to by 'paper', links to other files and small embed of video)
video (large embed of the video, links to other files)
