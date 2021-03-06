---
layout: slides
title: "CBSD, Isolation manager"
date: 2018-02-03
author: Goran Mekić
email: meka@tilda.center
youtube: CbIqBKRm-xQ
---
## How to manage jails, bhyve VMs and Xen via CBSD, while keeping it all simple

CBSD is able to manage bhyve, jails and xen on a cluster of hosts while keeping dependencies reasonably low. It is able to configure network interfaces and firewall rules dynamically, whether you use PF, IPFW or IPFILTER. This talk will cover main CBSD features, implementation details, future plans and growth of CBSD as well as ecosystem around it.

Management of Xen, VMs and jails on FreeBSD becomes increasingly tedious job especially with technologies like ZFS and VNET (just to mention few) which add on the number of alternative ways one can run FreeBSD based infrastructure. Combining that with multiple options for a firewall and the requirement for VMs to connect to jails and vice verse, makes FreeBSD very versatile. It is also very hard to choose the right set of tools. CBSD strives to unify management of jails and VMs while not taking away any options, and keeping UI and code simple as possible.
