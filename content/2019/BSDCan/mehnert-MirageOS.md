---
layout: slides
title: "MirageOS: minimizing the attack surface and vectors of network services"
date: 2019-05-18
author: Hannes Mehnert
email: hannesm@mastodon.social
venue: BSDCan 2019
---
How to reduce complexity in services, and enable laymen to run their infrastructure

Hypervisors are these days in lots of BSDs - BHyve on FreeBSD, VMM on OpenBSD - and provide fast and strong isolation, backed by hardware support, of virtual machines. In this talk, I'll introduce [MirageOS](https://mirage.io), which is a library operating system targeting these hypervisors amongst others. Each MirageOS "unikernel" is a single service (e.g. DHCP server, DNS resolver, Webserver) that only contains the libraries required for the service - a DNS resolver does not need a file system implementation. Each unikernel is tailored at compile time from a large ecosystem of reusable libraries.

For example, a MirageOS HTTPS unikernel is only 4% of the lines of code of an behaviorally equivalent UNIX-based service. In addition to this drastic reduction of the attack surface, MirageOS is implemented in the high-level functional programming language OCaml, which avoid spatial and temporal memory safety problems. MirageOS started more than a decode ago in Cambridge (UK), and is mostly ISC/MIT licensed.

MirageOS started as a research project targeting the hypervisor Xen, but has since then been ported to a variety of hypervisors, FreeBSD BHyve and OpenBSD VMM are supported since mid 2018. In addition to a tiny virtual machine, the [solo5 project](https://github.com/solo5/solo5) has minimized the monitor process in the host system (e.g. on FreeBSD the bhyve cli), which fits into ~2000 lines of code. Another target is a "standard" virtual machine which complies with the virtio interfaces and can be executed in existing orchestration systems.

I will talk about a MirageOS DNS server which I developed from scratch in recent years and run for several domains in detail, including a detailed look into the trusted code base of the running system, performance characteristics, monitoring, orchestration, and how to secure the supply chain. The design of MirageOS does not include process management, neither virtual memory - everything is executed in a single address space with cooperative multitasking in mind, we rely on the programming language for isolation properties between libraries. There are several approaches for formally verifying OCaml/MirageOS.

The programming language OCaml has a strong and static type system - which discovers lots of programming errors at compile time, and OCaml comes with an expressive module system, which we leverage to develop each unikernel agnostic of the deployment target. We usually develop unikernels on UNIX with smooth integration into existing debugging and profiling frameworks, and when we deploy, we use the same application code, but compile it for a different target - which imposes usage e.g. of the target-specific network device. Apart from basic Internet Protocols (DHCP, ARP, TCP, DNS), we developed a TLS stack for security and authenticity, and for persistency a reimplementation of the git protocol, which is compatible with the existing git. In 2018, we developed a MirageOS CalDAV server.

I'm member of the MirageOS core team and contribute to MirageOS since more than 5 years.

Links:

* [MirageOS website](https://mirage.io/)
* [MirageOS GitHub repository](https://github.com/mirage/mirage)
* [Not quite so broken TLS -- our design and implementation of a TLS stack](https://nqsb.io/)
* [nqsb-TLS Usenix 2015 paper](https://usenix15.nqsb.io/)
* [Network Semantics - a formal model of TCP/IP in HOL4](https://github.com/rems-project/netsem)
* [Robur - non-profit doing commercial MirageOS services](https://robur.io/)