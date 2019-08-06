---
layout: slides
title: "A Deep Dive into FreeBSD's Kernel RNG"
date: 2017-09-09
author: W. Dean Freeman and John-Mark Gurney
youtube: A41cDCE6pTc
---
Deep Dive into FreeBSD's Kernel RNG walks through the entire chain, from initializing the entropy subsystem at boot through delivery to userland applications via random devices, sysctls or APIs such as arc4random. It includes an evaluation of how entropy is collected for use while the system is running. The paper includes an evaluation of how the different RNG pools are loaded, as well as empirical measurements of the quality of entropy being fed into the PRNG in keeping with NIST's SP800-90A assessment methodology.
