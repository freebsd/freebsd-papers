---
layout: slides
title: "Use Dummynet to explore space, QUIC!"
date: 2021-09-19
author: Tom Jones
email: thj@freebsd.org
youtube: A2gmtkLMPf8
---

The Internet has grown vastly in the last 24 years, connection speeds have grown
from tens of kilobits a second up to hundreds of gigabits and we have changed
our core protocols from plain text to actively protecting privacy.

Our connection technologies have changed wildly too, no longer can we assume
that a user connecting is using a dial up modem over wet string, instead links
vary from wildly from 3G to gigabit FTTP hookups to geostationary orbits and out
to satellite whizzing around just above the ISS.

The software we develop and the network protocols we use need to be designed to
take into account this wide of link technologies. To do this we can still use
FreeBSD’s old faithfully network emulator, Dummynet. Dummynet has been core to
evaluating the satellite performance of the absolute latest Internet protocol,
QUIC.

This talk will provide and introduction to Dummynet and how it can be used to
emulate satellite links, 4G/5G links and others, and the role it can have in the
future evolution of the Internet.

**Tom Jones**

Tom Jones is an Internet Engineer and Researcher from the Shining Granite City
of Aberdeen in Scotland. He is a contributor to the IETF and has written RFCs
documenting the UDP API, increasing the MTU in the Internet and most recently
been exploring the practicalities of using QUIC on satellite links. In the last
year he has been tricked into running virtual conferences and hosting the
excellent BSDNow news show. For reasons unknown he chooses to run and cycle
ultra endurance distances.
