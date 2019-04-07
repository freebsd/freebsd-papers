---
layout: paper
title: "Finalizing booting requirements for a guest running under bhyvearm"
date: 2019-03-24
author: Nicolae-Alexandru Ivan, Mihai Carabas
email: nicolae.ivan@stud.acs.upb.ro.ro, mihai.carabas@cs.pub.ro
paper: carabas-Finalizing_booting_requirements_for_a_guest_running_under_bhyvearm.pdf
---
Keeping track of time is an invaluable resource in modern software systems. The vast majority of existing CPUs posses various clocks and timers in order to accommodate time related mechanisms required by software. These same needs apply to virtualized environments, where the guest operating system uses time based events. To this end, a virtualized timer is required. This research project describes implementing such a timer in FreeBSD for the ARMv7 architecture.
