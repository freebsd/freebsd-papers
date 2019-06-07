---
layout: slides
title: "Preparing your home router(s) for the future: A journey through Homenet and interconnected objects"
date: 2018-06-09
author: Massimiliano Stucchi
email: max@stucchi.ch
youtube: LeGQd_R-G-M
---
This talk is about the Home Networking Control Protocol (RFC7788) and how these specifications can be used to create a future-proof, IPv6 compliant SOHO router.

Almost two years ago, RFC7788 introduced the Home Networking Control Protocol - also called homenet - which "enables discovery of network borders, automated configuration of addresses, name resolution, service discovery, and the use of any routing protocol that supports routing based on both the source and destination address." Many routers in SOHO environments nowadays run different forms of BSDs, prominently being OpenBSD and FreeBSD under the hood of a PFSense install. Homenet's focus is specifically on IPv6-enabled networks, although support for IPv4 is also included.

Homenet introduces many new functionalities in a home network, and makes it easy for devices to interconnect, making it a better platform to support the IoT now and in the future.

In this talk, I will discuss all the services and protocols involved in the homenet specifications and documents, and will outline how these can be integrated into the BSDs by showing configurations for OpenBSD and FreeBSD.
