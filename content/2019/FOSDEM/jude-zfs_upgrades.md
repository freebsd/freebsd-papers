---
layout: slides
title: "ZFS Powered Magic Upgrades"
date: 2019-02-02
author: Allan Jude
email: allanjude@freebsd.org
youtube: YcdFln0vO4U
---
## Using boot environments for atomic in-place upgrades

Describe a system of using ZFS Boot Environments to quickly, safely, and atomically upgrade 100s of remote machines.

### Overview:
* How the file system hierarchy is modified to allow the systems to be upgraded in-place
* How we use ZFS to create and deploy the boot environments
* Simplifying the creation of the BEs using poudriere image
* Extending poudriere image to support ZFS
* Using zfsbootcfg to boot a new BE once
* How we determine if the BE "works" and should be promoted to the default

### Motivation:
* We often have only SSH access to the machines, so we needed something that could self-recover just by power cycling the machine
* No longer need to use freebsd-update, mergemaster, or etcupdate
