---
layout: paper
title: Advanced VPN support on FreeBSD systems
date: 2002-11-16
author: Riccardo Scandariato
email: scandariato@polito.it 
---
Currently, the VPN support offered by FreeBSD is quite limited: it provides a way to establish tunnels but it does not consider the problems of multiple VPNs concurrently deployed on the same machine. Our implementation enables the provisioning of VPN services on FreeBSD by extending its routing capabilities. Primarily, our implementation provides support for multiple IP routing tables (one for each VPN) in order to avoid conflicts between overlapping address spaces of different VPNs. User-space programs (route, zebra, etc) can select the proper instance when accessing/updating a routing table through a modified routing sockets interface. At the kernel level, the different VPN flows are identified on per-interface basis. Once a packet is recognized as belonging to a given VPN, the forwarding routine selects the proper routing table to look up. We also modified several user-level applications to allow the exploitation of the new routing infrastructure, such as "route", "netstat", "zebra", and "ifconfig".