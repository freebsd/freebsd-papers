---
layout: slides
title: "Why I prefer thick jails over thin jails"
date: 2019-09-22
author: Dan Langille
email: dvl@freebsd.org
youtube: kAJ7RzfPaLA
---
Jails have a long history on FreeBSD.  [ezjail](http://erdgeist.org/arts/software/ezjail/) came along and used a shared basejail for all the jails. Upgrade that jail, and you’ve upgraded all the jails. It was wonderful, convenient, and fast.

After a few upgrades between major versions, the author discovered he hadn’t been runing mergemaster on all those jails for all those years. Useful new features were unavailable, such as include on newsyslog.conf(5). Much time was spent doing mergemaster on many jails.

Furthermore, if you upgraded the basejail, you really need to upgrade all the jails or you’d get stuff failing to run properly.

There is more than one jail manager on FreeBSD. The author has also used [iocage](https://iocage.readthedocs.io/en/latest/index.html) and likes each of for different reasons. When he decided to convert a server from ezjail to iocage, the [existing script](https://iocage.readthedocs.io/en/latest/install.html#migrating-from-ezjail-to-iocage) did not work, so he wrote a new one. He has since used it to convert two servers and has plans for two more.

Now, the upgrades between major versions are relatively eaiser, but can be managed on a need-to-do basis. The host can be upgraded one day, and the jails left for weeks, or in the author’s case, months later.

Learn from his mistakes, come see thin-to-thick.

This talk will cover:

* short introduction to jails
* brief overview of ezjail and iocage
* why convert from thin to thick
* the problems solved by the new script
* why thick is not for you
* when thin is better
* monitoring tips to track vulns in your jails
* why you should never use jail managers
* why you should always a jail manager
* why etcmerge is something you should know about

After hearing this talk, you will know how to convert a thick jail to a thin jail and wonder why you never did this before. Your system upgrades will be easier, and your jails will be more robust.

**Dan Langille**

Dan Langille first started with Unix-like operating systems sometime in the early 1980s. In 1998, he discovered FreeBSD on a near-daily basis after needing a firewall for his ADSL connection. From that start, he began several online journals, founded two highly successful open source conferences, and eventually turned his hobby into a profession.

Dan now works as a sysadmin for a widely-known infosec company and is frequently impressed by those he works with.

When not running conferences or working, Dan blogs about this activities. He wishes he did more mountain biking.
