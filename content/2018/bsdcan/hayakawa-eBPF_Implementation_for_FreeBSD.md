---
layout: slides
title: "eBPF Implementation for FreeBSD"
date: 2018-06-08
author: Yutaro Hayakawa
email: yhayakawa3720@gmail.com
youtube: 4vGZm2qlEBY
paper: hayakawa-eBPF_Implementation_for_FreeBSD.pdf
---
This talk introduces a work-in-progress implementation of the eBPF(Extended Berkeley Packet Filter) for FreeBSD. First we show an overview of Linux's eBPF system structure and how we implemented that on FreeBSD. After that, we demonstrate how it is useful for the FreeBSD with some concrete use cases such as fast and flexible packet processing with eBPF-enabled VALE/mSwitch software switch with some performance number.

eBPF is an in-kernel virtual machine with an independent 64-bit instruction set architecture with C calling convention. It was appeared in the Linux kernel in 2014 as an extension to the existing BPF. Compared to the classic BPF, the instruction set is extended to make it a highly-flexible domain-specific language. Although BPF was originally designed for packet classification, eBPF in Linux is used as a building block of data processors which require complexity and flexibility. Today many applications such as dynamic tracing, resource control, and system call filtering are proposed and implemented by using eBPF in Linux. In the network community this is hot technology for programming high performance network packet processor including in-kernel packet processing framework like XDP, software switch like OpenVSwitch or even NICs like Netronome NFP.

We will break up existing Linux eBPF system into several components and explain how each component works. It makes clear what should be implemented when porting it to FreeBSD, what design choices are available and what we need to concern from security point of view.