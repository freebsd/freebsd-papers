---
layout: video
title: "All along the dwatch tower: A DTrace tool for the masses"
date: 2019-06-08
author: Devin Teske
email: dteske@FreeBSD.org
youtube: xqOl_HY86n8
---
I would like to present a new utility called dwatch that I added to FreeBSD 12.0-CURRENT.

Using dwatch, in this talk you will learn how to:

* Watch processes entering system CPU scheduler
* Print arguments being passed to functions
* Easily watch multiple probes simultaneously
* Globally watch all function traversal from every process/thread
* Filter output by user or group, including the ability to use regex
* Watch jail activity
* Use patterns or regular expressions to match on executable name(s), pid, etc.
* Look for a particular path being created, removed, accessed, etc.
* Watch interprocess communication signaling
* Log network data events
* Schedule timed samplings for events of interest
* Dump process trees for processes triggering a probe
* Watch child processes
* Show commands being executed in realtime
* Write modules to centralize logic into easy-to-access profiles
* Share modules with each other and help your community
* More...

With dwatch, using DTrace has never been so fun and painless.

FreeBSD Differential: https://reviews.freebsd.org/D10006