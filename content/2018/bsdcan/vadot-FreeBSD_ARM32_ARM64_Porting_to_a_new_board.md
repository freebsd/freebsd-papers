---
layout: slides
title: "FreeBSD ARM32/ARM64: Porting to a new board"
date: 2018-06-09
author: Emmanuel Vadot
email: manu@FreeBSD.org
youtube: YoB5NknHWbk
---
While porting FreeBSD to a new architecture can be hard and requires a lot of knowledge of a lot of the kernel subsystem, porting to a new board is much easier. We will take the Rock64 board from Pine64 for the exercise of porting FreeBSD to it and see what it take to have kernel booting for the first time and what are the next step when porting to a new SoC. Even if the Rock64 is an ARM64 board the step are the same for an ARM32 one.

During this talk you will learn what steps are needed for porting FreeBSD on a new ARM32/ARM64 board. We will take the Rock64 as an example for ARM64 and, if time permit, the Tinker board for ARM32. We will start by looking at resources on the board to make a list of task to do. Then we will look at how boot the FreeBSD GENERIC kernel on the board to see if we can, without SoC specific drivers, at least boot to multiuser mode. And finally we will see how to make a clock driver to allow kernel modules to enable/disable the component of the SoC.