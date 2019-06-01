---
layout: video
title: "Introducing FreeBSD/VPC: Hosting Virtual Private Clouds on FreeBSD"
date: 2018-06-08
author: Sean Chittenden
email: seanc@freebsd.org
youtube: La4ekkKbM5o
---
This talk presents this collection of enhancements required to provide Virtual Private Clouds using FreeBSD. We will walk through some of the problems seen with running FreeBSD as a hypervisor, the kernel modifications required to provide performant bhyve guest networking, and the required userland administrative interfaces required to stitch together a working VPC based on FreeBSD/VPC.

bhyve is a useful compute platform for delivering guests using FreeBSD as a hypervisor, but limited by the networking virtualization stack in FreeBSD.

FreeBSD/VPC brings cloud networking semantics to FreeBSD administrators. FreeBSD/VPC is a suite of kernel modules that provides performant and highly configurable networking for bhyve guests. With the use of a new kvirtio_net backend for bhyve guests and a new suite of VXLAN-related network interfaces, it is possible to provide >30Gbps of encapsulated network throughput between Linux VMs running on top of FreeBSD.

While the configuration and management of virtual routing tables has been possible, it has been complex and not practical at scale. Along with new kernel interfaces, many enhancements to the usability of FreeBSD's network virtualization layer have been made to allow for simple administration of VXLAN.

This talk presents this collection of enhancements and walks through some of the problems seen with running FreeBSD as a hypervisor, the kernel modifications required to provide performant bhyve guest network performance, and the userland administrative interfaces required to create a VPC.