---
layout: paper
title: Authorization and charging in public WLANs using FreeBSD and 802.1x
date: 2002-06-14
author: Pekka Nikander
email: pekka.nikander@ericsson.com
---
The IEEE 802.1x standard defines a link-layer level authentication protocol for local area networks. While originally designed to authenticate users in a switched Ethernet environment, it looks like the most important need for 802.1x lies in wireless networks, especially IEEE 802.11b based Wireless LANs. Furthermore, due to the flexibility of the Extensible Authentication Protocol (EAP), the heart of 802.1x, it looks like 802.1x could be used for many purposes its original designers have not foreseen.
In this paper, we describe an FreeBSD-based open source 802.1x implementation, and show how it can be used to implement different authorization and charging systems for public WLANs, including a pre-paid, pay-per-use charging system and another one based on community membership. The implementation is based on the netgraph facility, resulting in a surprisingly flexible and simple implementation. 
