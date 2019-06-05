---
layout: video
title: "Imprisoning software with libiocage: Utilizing FreeBSD to build secure compartments"
date: 2018-06-09
author: Stefan Grönke
email: stefan@gronke.net
youtube: CTGc3zYToh0
---
Iocage is a FreeBSD jail manager based on ZFS that heavily uses operating system features to define and maintain userland compartments. Each compartment can have constrained access to filesystem, network and system resources.

This talk tells the story of libiocage, a Python library and commandline tool made for programmatic usage, security, stability and performance. We will explore the reason for yet another version of iocage, question design choices and look in the future of the project.

A practical view on the command line client and Python interfaces is taken to outline key concepts while quickly diving into advanced use cases that satisfy paranoia and invite for automation.

libiocage is a jail management library following the iocage approach. The project started about one year ago as Pull-Request on the Python implementation of iocage to make the tool accessible for Python programmers. Initially this was required to reliably reproduce a kernel crash in VNET by spawning massive amounts of jails - since then the project evolved and moved forward to be compatible with jails from all previous versions of iocage with an object oriented Python 3 implementation.

The project aims for secure, reliable and efficient management of jails that system administrators and DevOps engineers may use to compartmentalize userland environments and their peripherals like network and storage access. The speed improvements introduced allow using it for socket-based activated jails and encapsulation of each individual command invoked in a shell. If this sounds boring, that's probably a good thing. In operations we have a lot of excitement, and the best way to weather it, is to have a solid tool.

At the time of writing the tool is moving towards alpha testing to collect user feedback that will be turned into integration tests.

libiocage on GitHub: https://github.com/bsdci/libioc
