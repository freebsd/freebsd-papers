---
layout: paper
title: "Managing System Images with ZFS"
date: 2019-03-23
author: Allan Jude
email: allan@klarasystems.com
paper: jude-Managing_System_Images_with_ZFS.pdf
---
The author describes existing procedures, tools, and ongoing development to improve the process of updating appliances, remote systems, and individual computers using ZFS. This paper describes a mechanism for replacing the operating system image with a newer image in a safe and atomic fashion. This system allows for fail-safe unattended upgrades of remote appliances and machines with a built in automatic recovery mechanism in the event of failure. Current and planned enhancements to 'poudriere image' are described as well as improvements to support tools including bectl and zfsbootcfg.
