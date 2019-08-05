---
layout: slides
title: "Towards Oblivious Sandboxing"
date: 2017-09-09
author: Jonathan Anderson
youtube: -0s1bCzUx0Y
---
Application compartmentalization (a.k.a., sandboxing) can be used to protect applications from themselves and protect users from misbehaving applications. However, the current state of the art requires applications to be willing participants: invasive modifications are required, and it's up to the application whether or not it will voluntarily sandbox itself. We would like to move towards a world in which applications can be started from within compartments (created with technologies like Capsicum) and have their access to global namespace like filesystems transparently mediated. This approach may never scale to applications with complex event models like web browsers, but we believe that there is a great deal of mileage to get out of it with more straightforward (though still sophisticated) applications like compilers.

This talk will describe recent work in FreeBSD that is driving at the goal of transparent, oblivious sandboxing. We will discuss changes in the ELF image activator and run-time linker to support transparent sandboxing as well as a support library for managing pre-opened directory descriptors and a simple shell application to start applications from within sandboxes. Together, these techniques allow us to take a few more steps towards our goal of usefully confining applications whether they like it or not.