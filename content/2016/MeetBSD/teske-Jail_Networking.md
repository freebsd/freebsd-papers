---
layout: video
title: "Jail Networking"
date: 2016-11-11
author: David Teske
email: dteske@FreeBSD.org
youtube: aoW7pWuhT_A
venue: MeetBSD 2016
---
Since their introduction to stable/4 in 1999, jails have given FreeBSD
lightweight containers. In 2008, the VIMAGE kernel option was introduced to
stable/8 for network virtualization. In 2009, the vnet option was introduced,
also in stable/8, to give jails their own network stack. Combined with the
power of ZFS, vnet jails are a useful tool to add to your toolbox. In this
talk we will cover:

* New tools and examples introduced in 2016
* Creating and managing vnet jails in stable/11
* Two types of network bridging: if_bridge and netgraph
