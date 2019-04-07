---
layout: paper
title: "bhyve - Improvements to Virtual Machine State Save and Restore"
date: 2019-03-24
author: Darius Mihai, Mihai Carabas
email: dariusmihaim@gmail.com, mihai.carabas@cs.pub.ro
paper: mihai-bhyve_Improvements_to_Virtual_Machine_State_Save_and_Restore.pdf
---
As more complex tasks are delegated to distributed servers, virtual machine hypervisors need to adapt and provide features that allow redundancy and load balancing. One such mechanism is the virtual machine save and restore through system snapshots. A snapshot should allow the complete restoration of the state that the virtual machine was in when the snapshot was created. Since the snapshot should encapsulate the entire state of the virtualized system, the guest system should not be able to differentiate between the moment a snapshot was created and the moment when the system was restored, regardless of how much real time has passed between the two events. This paper will present how the time management and block devices are saved and restored for bhyve, FreeBSD's virtual machine hypervisor.
