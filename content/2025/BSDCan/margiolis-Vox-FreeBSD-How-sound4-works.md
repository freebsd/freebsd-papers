---
layout: slides
title: "Vox FreeBSD: How sound(4) works"
date: 2025-06-14
author: Christos Margiolis
---

FreeBSD's audio subsystem, sound(4), is one of the fastest out there, but is
rather unknown and until recently was largely unmaintained. This talk will go
through the various components of sound(4) that make sound possible on FreeBSD,
that is:

- The generic driver's structure, control flow and interaction with the device
  drivers.
- The audio processing chain.
- The user-facing interfaces for interacting with the sound system.

The talk will also mention some notable recent, ongoing and future work across
the whole sound system, since my taking over of its development.

I also intend to showcase examples of:

- Audio driver and application develpoment on FreeBSD.
- FreeBSD being used for music production, and why a musician would consider it
  instead of other operating systems.
