---
layout: slides
title: "pkgbase: Are we there yet ???"
date: 2019-09-22
author: Emmanuel Vadot
email: manu@freebsd.org
youtube: Wp4u-SoJw1g
---
pkgbase on FreeBSD is the method currently developed to handle base installation and update/upgrade with pkg(8). It was started by Baptiste Daroussin (bapt@) a few years ago and first presented in BSDCan 2015 (see https://www.bsdcan.org/2015/schedule/events/563.en.html). It was also planned to be included in 12.0-RELEASE but this didn’t happened.

I recently revive the work since I needed to create an appliance with an installer and an update system. Of course it didn’t work out of the box and I had a lots of issues, some known, some not known. We will see all the remaining issues when I started working on it, from config file to bsdinstall(8) support and multiple kernel installation. Since this is an ongoing effort all those issues will be hopefully resolved by the time this presentation is happening.
