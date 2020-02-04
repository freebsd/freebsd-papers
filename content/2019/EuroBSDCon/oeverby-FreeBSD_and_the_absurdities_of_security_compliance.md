---
layout: video
title: "FreeBSD and the absurdities of security compliance"
date: 2019-09-22
author: Eirik Øverby
email: eirik.overby@modirum.com
youtube: I2rhwnY6Bg4
---
Assume absurdity, embrace sanity. Welcome to The Blame Game.

The world of security compliance is defined by a few key players: The ones writing the requirements, the ones covering their asses, and the ones who’ll be blamed in the end. Since about 2008 we’ve been firmly placed in the latter category, and despite the obvious downsides it is, really, where we prefer to be.

Security requirements pertaining to the payment industry include the various PCI standards, card system specific requirements, national and regional laws, regulations and directives, and whatever else comes to the minds of the various players. While there is sanity to be found in some of them, there is also plenty of absurdity. It is this, above all, that leads us to use the term “The Blame Game” about it all.

We do pretty much everything with FreeBSD. From routers (bsdrp) and firewalls (pfSense) to application- and database servers, we’re running FreeBSD everywhere. The only closed-source software we employ are our own applications (boo!). Our basic principle has always been to identify the root cause of a security requirement and then comply in a way that goes beyond “ticking the box”; whatever we do has to be useful and practical – and not something we’re ashamed to talk about.

What we want to show:

* Compliance is much harder than security but not because the tools can’t do it
* Open Source, and FreeBSD, CAN be used to achieve compliance in the payment industry
* If you implement sane security measures, compliance is nearly free 
* The hardest part is explaining what you’ve done and why

**Eirik Øverby**

Slackware-gone-BSD in the early 00s, escaped the dying world of OS/2 to be doomed to death by Netcraft for another decade. Now managing jailed (but not dead!) systems for a living and as a hobby.
