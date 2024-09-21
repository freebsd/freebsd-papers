---
layout: slides
title: "1-800-RC(8)-HELP: Dial Into FreeBSD Service Scripts Mastery!"
date: 2024-09-21
author: Mateusz Piotrowski
---

The presentation delves deep into the rc(8) service scripts. We will begin by
analyzing the service script framework in FreeBSD, which is built around rc(8)
and rc.subr(8), and take a closer look at some of the most recent additions.
Next, we will not only discuss common patterns used to implement different
kinds of service scripts (i.e., the scripts residing in rc.d directories) but
also examine unusual and complex scripts in detail. Additionally, we will
explore all the most relevant parts of the rc(8) subsystem, such as rc.conf(8),
rcorder(8), sysrc(8), and service(8). As a result, you should be able to easily
design, implement, debug, and maintain FreeBSD service scripts.
