---
layout: paper
title: "Yet Another Container Migration on FreeBSD"
date: 2019-03-24
author: Yuhei Takagawa, Katsuya Matsubara
email: g2118021@fun.ac.jp
paper: takagawa-Yet_Another_Container_Migration_on_FreeBSD.pdf
---
The container-based virtualization, that multiplexes and isolates computing resource and name space which operating system (OS) provides for each process group of application, has been recently attracted. We focus on container migration among machines since it is one of the most important technology for realizing load balancing and increasing availability in cloud computing, that is a major application of the virtualization. Although FreeBSD VPS has already implemented one kind of migratable containers in FreeBSD, it is not enough in terms of resource limitation, compared to Linux one. This paper shows a novel implementation that how resource limitation and isolation close to that of Linux can be realized for FreeBSD containers. We also explain how processes, which could have sessions of file open and network connection, running in a FreeBSD container can be checkpointed and then they can be restored in another container. This implementation bases on runC which is one of standard container runtime and CRIU which is a major process migration tool in Linux.
