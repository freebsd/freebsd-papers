---
layout: slides
title: "Configuring build base on FreeBSD"
date: 2018-02-03
author: Rober fern
email: 
youtube: di79HpcMaXI
---
## Making things easy for the user

FreeBSD has some knobs to set in order to build the base system or to avoid building some parts of the system. This way the build process could be optimized to avoid wasting time.

With this procedure, the user has an easier way of configuring how to build the target system

The first implementation allows the user to set, unset and check the dependencies of the option that can be set to build the base system. Lots of users uses this kind of options to speed up the process of building the base system but there are some dependencies that might not be taken into consideration and the user could realize of this changes when the build process is finished, wasting a lot of building time.

More than a lecture about this approach, this event is meant to be a demonstration of "how can it be done".
