---
layout: slides
title: Building a FreeBSD Appliance With NanoBSD
date: 2005-11-26
author: Poul-Henning Kamp
email: phk@freebsd.org
---
An appliance in this context is a computer which can be stuck in
an attic, nailed to a wall and forgotten about.  If there is problems
with it, you can power cycle it and it will start again.  Every
time.

Appliances can do many different things:  Firewalls, access points,
data collection, industrial control, network monitoring and so on.

It should of course be possible to update the software remotely and
if the new version doesn't fail, it should be possible to return
to the old software version again.

NanoBSD is a way to build FreeBSD for use in such appliances.

