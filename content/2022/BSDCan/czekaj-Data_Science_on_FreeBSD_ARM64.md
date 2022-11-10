---
layout: slides
title: "Data Science on FreeBSD/ARM64"
date: 2022-06-03
author: Maciej Czekaj
youtube: NxON0Fv28LE
---
Recently, ARM64 became a Tier I platform for FreeBSD. This talk is a report from a Data-Scientific experiment run on the ThunderX2 ARM server platform under FreeBSD/12. The experiment was using a mix of a custom C++ simulator and FOSS software (Pandas, SciPy, etc…). This large SMP system (56 cores) with lots of RAM was put under constant high load for weeks until it produced the final results, giving testimony to the stability of the FreeBSD/ARM64 platform. The talk discusses the experience from porting the software suite from Linux and ensuring its robust operation under constant memory pressure.
