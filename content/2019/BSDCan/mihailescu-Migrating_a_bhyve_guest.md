---
layout: slides
title: "Migrating a bhyve guest"
date: 2019-05-17
author: Elena Mihailescu
email: elenamihailescu22@gmail.com
---
Nowadays, servers have become more and more used, whether we talk about providing web services and resources or parallel and distributed processing. In order to ensure load balancing or continuous functionality even if a cluster's node will be removed (for replacement or for improvement), a system administrator may use a migration mechanism.

Even though necessary, bhyve does not have a migration feature implemented. In this presentation, I will present some migration features for bhyve based on a state save and restore mechanism for bhyve.

Virtual machine migration is a powerful tool when talking about server maintenance. Well known hypervisors, such as Xen, kvm and VMWare, have migration mechanism for moving a virtual machine from a host to another. However, bhyve, FreeBSD's hypervisor does not, even if this feature's importance seems to be growing each day.

In the following presentation, we will show three ways of migrating a guest where subsequent types will provide lower downtime. These three migration algorithms are still under development in a project started at University Politehnica of Bucharest and are implemented using a state save and restore mechanism that is under development at the same university.

The first migration method is not a conventional method of migrating a guest, but it may be used. This procedure suspends the virtual machine state and restores it on another host based on the files that contain the guest's state. The second migration approach is a warm migration algorithm where the guest is suspended and its memory and state are migrated via a socket to the destination host. At the destination host, the guest is started based on the received state. The third one is the live migration approach.

A live migration feature for bhyve is the most difficult type of migration to implement because it requires migrating the guest memory in rounds. In each round, the memory that has been modified since the previous round started has to be detected and sent to the destination. The procedure of memory modification detection between two rounds is itself a challenge when talking about live migration. In the presentation, we will describe a method of detecting the differences between two migration rounds based on FreeBSD's Copy-on-Write mechanism and we will show why it cannot be applied to bhyve. Based on the previously described approach, we will present another memory modification detection algorithm that uses a dirty bit and the current implementation in bhyve.