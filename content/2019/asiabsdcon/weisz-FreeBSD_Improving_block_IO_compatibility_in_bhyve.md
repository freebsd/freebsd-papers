---
layout: paper
title: "FreeBSD - Improving block I/O compatibility in bhyve"
date: 2019-03-24
author: Sergiu Weisz, Mihai Carabas 
email: sergiu121@gmail.com, mihai.carabas@gmail.com
paper: weisz-FreeBSD_Improving_block_IO_compatibility_in_bhyve.pdf
---
## FreeBSD - Improving block I/O compatibility in bhyve

In a world where cloud computing and cloud infrastructures have become a mainstay, virtualization technologies have enabled a secure way to share resources with different users. A snapshoting mechanism is of great use in the area of virtualization, as it enables the backup of virtual machines, or the creation of templates for machine state replication. These virtual machines have many different virtual devices connected to them that need to have their state saved and restored for a system to be truly useful; examples include block devices, USB devices, or system time. For block I/O a virtual machine may use different types of files depending on its use case. This leads to a greater flexibility in terms of features; for example, one can use a file type that enables saving the state of the hard disk in order to be used later, or as a backup. Hypervisors like VirtualBox, VMWare and Hyper-V already have support for multiple disk file formats. This paper will present a way to implement support for the devices mentioned above, and fill readers in on the procedure of saving device states.
