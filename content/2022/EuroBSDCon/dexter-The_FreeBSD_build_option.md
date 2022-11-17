---
layout: slides
title: "The FreeBSD build option, OpenZFS, bhyve, compat_linux, and jail.conf.d nexus"
date: 2022-09-18
author: Michael Dexter
youtube: -qFG8LebHvo
---
A powerful whole that is far greater than the sum of its parts  

FreeBSD 13.1 marks a milestone that was decades in the making: The unification of functioning build options that control operating system features, the cross-platform OpenZFS file system and volume manager, the configuration file format for the bhyve hypervisor, a Linux compatibility layer, and the Jail container subsystem with jail.conf.d which can efficiently enhance the security of them. No other open source or proprietary operating system can match these features and this talk will describe how FreeBSD 13.1 onward can provide the platform for flexible and secure compute environments that embrace a "learn once, deploy for decades" philosophy.

Available features of this stack include:

* Host and Container OS upgrades via OpenZFS snapshots
* Institutionally-contained Virtual Machines
* Lightweight and full-featured FreeBSD Virtual Machines
* Lightweight and full-featured FreeBSD Containers
* Lightweight and full-featured Linux and other OS Virtual Machines
* Lightweight and full-featured Linux Containers
* Virtual Machine management using popular Jail management tools

All using in-base or near-base tools.

This talk is aimed at new and moderately-experienced system operators thanks to its leveraging of in-based tools and documentation.
