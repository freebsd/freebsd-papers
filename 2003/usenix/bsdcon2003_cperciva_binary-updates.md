---
layout: paper
title: An Automated Binary Security Update System for FreeBSD
author: Colin Percival
email: cperciva@freebsd.org
slides: /_assets/bsdcon2003_cperciva_binary-updates.pdf
---
With the present trend towards increased reliance upon computer systems, the provision and prompt application of security patches is becoming vital. Developers of all operating systems must generally be applauded for their success in this area; systems administrators, however, are often found lacking.
Anecdotal evidence suggests that for FreeBSD much of the difficulty arises out of the need to recompile from thesource code after applying security patches. Many people, after spending years using closed-source point-and-click operating systems, find the concept of recompiling software to be entirely foreign, and even veteran users of open source software are often less than prompt about applying updates. Providing these people with a binary option should significantly improve the rate at which security updates are applied.
This paper describes an automated system for building and distributing binary security updates for FreeBSD, and describes the challenges encountered. I also describe some of the limitations of this system, and discuss some possibilities for future work.
