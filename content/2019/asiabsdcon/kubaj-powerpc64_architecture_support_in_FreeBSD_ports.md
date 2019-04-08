---
layout: paper
title: "powerpc64 architecture support in FreeBSD ports"
date: 2019-03-23
author: Piotr Kubaj
email: pkubaj@anongoth.pl
paper: kubaj-powerpc64_architecture_support_in_FreeBSD_ports.pdf
---
IBM POWER processors are 64-bit CPU’s designed primarily for server market. With POWER9, there has been renewed interest in them, due to the use of open-source firmware and focus on security and control of the hardware. There are also new desktop boards with POWER9. Because of that, support for them has been recently greatly improved in FreeBSD with increased driver compatibility and more 3rd party software having available. For my project, I build the whole ports tree using Poudriere and fix the compilation errors I meet. In this paper, I specify challenges met during porting software to work on POWER processors on FreeBSD and show how most problems can be solved. FreeBSD on POWER architecture runs in big-endian variant only and uses old toolchain – with GCC 4.2 and binutils 2.17. This is why many problems are related to fixing bugs in big-endian variants of code and solving issues related to the old toolchain that the operating system uses.
