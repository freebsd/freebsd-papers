---
layout: slides
title: "Profiling the FreeBSD kernel boot: From hammer_time to start_init"
date: 2018-06-08
author: Colin Percival
email: cperciva@tarsnap.com
youtube: HMywejyXB9k
paper: percival-Profiling_the_FreeBSD_kernel_boot.pdf
---
I will describe work I did to profile the FreeBSD kernel boot - both adding instrumentation to the kernel to collect data while the system is booting, and converting the resulting timestamp records into a graphical visualization of where time is spent in the boot process. I will show results from some systems and highlight places where it is clear that the performance of the FreeBSD boot process can be improved.

Many users have complained over the years about the time it takes for FreeBSD to boot, but little work has been done until now to investigate this. Unfortunately it is difficult to profile the very beginning of the FreeBSD boot process; as a result, in late 2017 I introduced a new "TSLOG" framework for recording timestamps at points in the kernel boot. I will explain why existing mechanisms were insufficient and how the TSLOG framework operates, and how I utilized the TSLOG framework to annotate key parts of the FreeBSD kernel boot process. Finally, I will explain the process of converting logged timestamps from the kernel boot into a "flame chart".

The audience is expected to be generally familiar with C, but an understanding of FreeBSD kernel internals will not be assumed.