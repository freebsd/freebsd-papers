---
layout: video
title: "SSH Key Management"
date: 2018-06-08
author: Michael W. Lucas
youtube: FVT7sepck68
---
SSH is arguably the most widely deployed systems administration tool. It's also arguably the least well configured. Many sysadmins already know how to disable passwords and chroot users, but when it comes to managing host and user SSH keys, we rely on manually copying files around. That's fine with three servers and two sysadmins, but not so good with three thousand servers and two hundred sysadmins.

We'll fill in those gaps.

SSH is arguably the most widely deployed systems administration tool. It's also arguably the least well configured. Many sysadmins already know how to disable passwords and chroot users, but when it comes to managing host and user SSH keys, we rely on manually copying files around. That's fine with three servers and two sysadmins, but not so good with three thousand servers and two hundred sysadmins.

This talk takes you through:

* Key file formats
* Distributing the host key cache to OpenSSH and PuTTY clients
* Distributing client configurations
* OpenSSH configuration for automatic deployment and cloud configuration
* Improving the security of known_hosts
* SSH keys for automation
* Building and deploying SSH Certificate Authorities

Attendees will leave understanding how to scale their SSH systems--and, more importantly, when to scale those systems to the next level.

Based on the book "SSH Mastery, 2nd Edition"