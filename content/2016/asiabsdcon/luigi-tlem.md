---
layout: paper
title: "TLEM, very high speed link emulation"
date: 2016-03-12
author: Luigi Rizzo, Giuseppe Lettieri
email: luigi@freebsd.org
youtube: rlVYdDzhBi4
---
In this work we discuss the limitations of link emulators based on conventional network stacks, and present our alternative architecture called TLEM, which is designed to address current high speed links and be open to future speed improvements. TLEM is structured as a pipeline of stages, implemented with separate threads and with limited interactions with each other, so that high perfor- mance can be achieved. Our emulator can handle bidi- rectional traffic at speeds of over 18 Mpps (64 byte pack- ets) and 30 Gbit/s (1500 byte packets) per direction even with large emulation delays. Even higher performance can be achieved with shorter delays, as the workload fits better into the L3 cache of the system. TLEM runs on any system that supports netmap (this includes FreeBSD, Linux and now even Windows hosts). The code is available as open source under a BSD license at [github.com:luigirizzo/tlem](https://github.com/luigirizzo/tlem). 
