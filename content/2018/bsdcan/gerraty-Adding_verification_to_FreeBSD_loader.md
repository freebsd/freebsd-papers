---
layout: slides
title: "Adding verification to FreeBSD loader"
date: 2018-06-08
author: Simon Gerraty
email: sjg@juniper.net
youtube: La4ekkKbM5o
---
Secure boot is a popular topic these days.

Junos (a FreeBSD based OS) has shipped with Verified Exec (from NetBSD) for over a decade, but there is a big gap between firmware power on and veriexec enforcement.

Adding the equivalent of verified exec to the loader addresses this gap.

Fixing the loader to verify modules and kernel has been on our roadmap for ages, but trying to squeeze enough of OpenSSL into the loader to handle verification of X.509 certificate chains, was simply not feasible.

Thomas Pornin's talk last year on BearSSL, changed the game. With this tiny library in hand I was able to add verification to the FreeBSD loader in a manner compatible with Verified Exec, while adding only about 100K to the size of the loader.

This talk will discuss the background, design decisions and implementation.