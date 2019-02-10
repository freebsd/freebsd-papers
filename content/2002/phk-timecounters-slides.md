---
layout: slides
title: "Timecounters: Efficient and precise timekeeping in SMP kernels"
date: 2002-01-01
author: Poul-Henning Kamp
email: phk@FreeBSD.org
---
The FreeBSD timecounters are an architecture-independent implementation
of a binary timescale using whatever hardware support is at hand
for tracking time. The binary timescale converts using simple
multiplication to canonical timescales based on micro- or nano-seconds
and can interface seamlessly to the NTP PLL/FLL facilities for clock
synchronisation.  Timecounters are implemented using lock-less
stable-storage based primitives which scale efficiently in SMP
systems. The math and implementation behind timecounters will be
detailed as well as the mechanisms used for synchronisation.
