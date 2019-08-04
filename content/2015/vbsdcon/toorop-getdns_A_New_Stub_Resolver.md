---
layout: slides
title: "Interesting Things You Didn't Know You Could Do With ZFS"
date: 2015-09-13
author: Willem Toorop
youtube: 73M7h56Dsas
---
getdns is a modern asynchronous DNS API. It implements DNS entry points from a design developed and vetted by application developers, in an API specification originally edited by Paul Hoffman. The open source C implementation of getdns is developed and maintained in collaboration by NLnet Labs, Verisign Labs, Sinodun and No Mountain Software. The presentation will demonstrate how the library gives fine grained access to DNS and DNSSEC, how this is an enabler for securely bootstrapping encrypted channels, and how this is especially applicable for system software. The library's stub resolution will be compared with the standard system stub, highlighting the improved control over underlying transport mechanisms. getdns library does its utmost best to get out of the way of applications by not imposing a modus operandi, but hooking into the applications way of handling I/O and memory management. This is illustrated by showing how getdns can hook into existing asynchronous event bases.
