---
layout: slides
title: "Using FreeBSD to Render Realtime Audio & Video"
date: 2003-09-11
author: John Baldwin
email: jhb@FreeBSD.org
paper: article.pdf
venue: BSDCon 2003
---
One of the largest selling points for The Weather Channel (TWC) is the
ability to generate localized content for its subscribers,
specifically local weather forecasts.  To facilitate this localized
content, TWC deploys smart devices in cable head ends.  These smart
devices are called STARs (Satellite Transmitter Addressable Receivers)
and are responsible both for collecting weather data and displaying
the data to the user in an audio and video presentation.

TWC decided to produce a next generation STAR that was more flexible
than the current generation as well as cheaper.  FreeBSD was chosen as
the platform for these devices.  Although FreeBSD was largely suitable
for this application, a few modifications were required and several
workarounds were employed.  The end result is a PC built mostly of
off-the-shelf components that is able to render broadcast quality
audio and video in realtime.
