---
layout: slides
title: "FreeBSD and NUMA"
date: 2015-06-03
author: John Baldwin
email: jhb@FreeBSD.org
venue: NYC*BUG
---
Newer x86 systems continue to scale horizontally by adding more cores
rather than vertically.  This in turn has placed additional strain on
other system components such as memory controllers.  The solution has
been to scale these components horizontally as well.  This results in a
more complex system requiring additional tuning for optimal
performance.

The first part of the talk will provide an overview of these extra-CPU
scaling changes in x86 systems.  We will also talk about the resulting
performance impacts and some of the tradeoffs to consider when tuning.

The second part of the talk will focus on changes to FreeBSD to
support these system changes both in past releases and anticipated
work in future releases.

Bring your facial tissues.  The problems here are similar to those of
achieving optimal performance on systems with multiple CPUs, and we
all know how well that has worked out.
