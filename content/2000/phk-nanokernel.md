---
layout: paper
title: The Nanokernel
date: 2000-01-01
author: [ "Dave L. Mills", "Poul-Henning Kamp" ]
email: [ "mills@udel.edu", "phk@FreeBSD.org"]
---
Internet timekeeping has come a long way since first demonstrated
almost two decades ago. In that era most computer clocks were driven
by the power grid and wandered several seconds per day relative to
UTC. As computers and the Internet became ever faster, hardware and
software synchronization technology became much more sophisticated.
The Network Time Protocol (NTP) evolved over four versions with
ever better accuracy now limited only by the underlying computer
hardware clock and adjustment mechanism.
The clock frequency in modern workstations is stabilized by an
uncompensated quartz or surface acoustic wave (SAW) resonator, which
are sensitive to temperature, power supply and component variations.
Using NTP and traditional Unix kernels, incidental timing errors
with an uncompen- sated clock oscillator is in the order of a few
hundred microseconds relative to a precision source. Using new
kernel software described in this paper, much better performance
can be achieved. Experiments described in this paper demonstrate
that errors with a modern worksta- tion and uncompensated clock
oscillator are in the order of a microsecond relative to a GPS
receiver or other precision timing source.
