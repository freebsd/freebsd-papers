---
layout: paper
title: Dummynet: A simple approach to the evaluation of network protocols
author: Luigi Rizzo
email: l.rizzo@iet.unipi.it
paper: /_assets/other1997_luigi_dummynet.pdf
---
Network protocols are usually tested in operational networks or in simulated enviroments. With the former approach it is not easy to set and control various operational parameters such as bandwidth, delays, queue sizes. Simulators are easier to control, but they are often only an approximate model of the desired setting, especially for what regards the various traffic generators (both producers and consumers) and their interaction with the protocol itself.
In this paper we show how a simple, yet flexible and accurate network simulator - dummynet - can be built with minimal modifications to an existing protocol stack, allowing experiments to be run on a standalone system. dummynet works by intercepting communcations of the protocol layer under test and simulating the effects of finite queues, bandwidth limitations and communcation delays. It runs in a fully operational system, hence alloing for the use of real traffic generators and protocol implementations, while solving the problem of simulating unusual enviroments. With our tool, doing experiments with network protocols is as simple as running the desired set of applications on a workstation.
A FreeBSD implementation of dummynet, targeted to TCP, is available from the author. This implementation is highly portable and compatible with the other BSD-derived systems, and takes less than 300 lines of kernel code.
