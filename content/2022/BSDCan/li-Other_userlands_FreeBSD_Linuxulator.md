---
layout: video
title: "Other userlands in the FreeBSD Linuxulator"
date: 2022-06-03
author: Charlie Li
youtube: WJXBWuHSejM
---
The FreeBSD Linuxulator is advertised as "allowing users to install and run unmodified Linux binaries." The ports tree has the linux-c7 collection based on CentOS 7 packages, well-documented in the Handbook. More recently, debootstrap emerged as an alternative to the CentOS userland, allowing for Debian or Ubuntu userlands. Having (advertised) options for userland choices gives inspiration for even more choices to emerge.

Prior to my FreeBSD adventure, my operating system of choice was Arch Linux. I liked its simplicity (to me) in configuration and maintenance despite some manual work in initial setup, so I wanted to go back to it for my Linuxulator usage. I will show how an Arch Linux userland works, particularly with the pacman package manager, and all of the warts that come with running more bleeding-edge Linux binaries compared to the other userlands. We will also discuss future directions and if different Linux libc implementations also work.
