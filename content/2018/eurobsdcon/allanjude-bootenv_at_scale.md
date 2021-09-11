---
layout: paper
title: "Using Boot Environments at Scale"
date: 2018-09-22
author: Allan Jude
email: allanjude@freebsd.org
---
**Abstract**: 
Describe the design of the system of boot environments deployed at ScaleEngine to quickly, atomically, and safely update 100s of remote FreeBSD servers.

Overview:
- How the file system hierarchy is modified to allow the systems to be upgraded in-place
- How we use ZFS to create and deploy the boot environments
- Simplifying the creation of the BEs using poudriere image
- Using zfsbootcfg to boot a new BE once
- How we determine if the BE "works" and should be promoted to the default

Motivation:
- We often have only SSH access to the machines, so we needed something that could self-recover just by power cycling the machine
- No longer need to use freebsd-update, mergemaster, or etcupdate

Future Work:
- Extending zfsbootcfg to detect repeated failures
