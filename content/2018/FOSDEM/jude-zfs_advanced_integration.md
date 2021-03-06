---
layout: slides
title: "ZFS: Advanced Integration"
date: 2018-02-03
author: Allan Jude
email: allanjude@freebsd.org
youtube: 1t9-w8SIcts
---
## Server, Laptop, Embedded, or Appliance -- ZFS is the Answer

How to apply various FreeBSD technologies and features in combination with ZFS to get the most out of a system, be it a Server, Laptop, Embedded, or an Appliance.

ZFS is an advanced filesystem, but that doesn't mean it is complicated or hard to understand.

After an overview of the basics of what ZFS is and how it works, we'll delve into how to integrate ZFS into a system or product. Topics to include: * Boot Environments and how to use them - new boot environment management tool and library from Google Summer of Code - case studies / use cases * Advanced Boot Configuration (zfsbootcfg/nextboot) - Boot the new system image only once - Fall back to previous version if new system image fails to stay up for 5 minutes three consecutive times * Automated Boot Recovery (Appliance style failover/failsafe) - Fall back to rescue image if system fails to boot repeatedly (required for environments like Amazon where there is no console) * GELI Encryption Support - Improvements to allow unattended booting * Appliance Upgrading with ZFS (including zpool checkpoints) - Create a checkpoint before upgrading an appliance, revert to checkpoint if upgrade is not completely successful. Checkpoints can undo things that a snapshot cannot, like renaming or destroying an entire filesystem.

Techniques discussed will be of interest to most everyone, from users and developers for laptops and servers, to appliance manufacturers, and embedded products.
