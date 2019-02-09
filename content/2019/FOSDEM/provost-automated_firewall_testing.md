---
layout: paper
title: Automated Firewall Testing
date: 2019-02-02
author: Kristof Provost
email: kp@FreeBSD.org
youtube: -WzTyggngNA
---

We're all convinced that automated tests are a good idea. For some applications
(e.g. grep, awk, cc, ...) this is very straightforward. Others are a lot harder
to test, for example firewalls. Typically testing firewalls takes two to three
hosts. One to send traffic, the firewall test host and one to receive traffic.
This makes automated test orchestration complex and brittle. This in turn means
that tests either don't get written, are difficult to write and/or suffer
random failures unrelated to issues in the firewall itself. Virtualisation has
made this all somewhat easier, but it's still fiddly and difficult to make
robust. It's also slow.

The new FreeBSD network stack virtualisation lets us build on the existing
jails system to build test setups, execute tests and clean up in mere seconds,
without any requirement for additional hardware, or even hardware
virtualisation support.

FreeBSD 12 will ship with network stack virtualisation (known as VIMAGE or
vnet). This is an important feature for many applications, one of which is
automated network stack and firewall testing. As of FreeBSD 12 PF fully support
VIMAGE, allowing users to configure a firewall for each jail.

This talk will introduce VIMAGE and show how it can be used to easily write
firewall tests. If there's time a few interesting bugs and their test cases
will also be discussed.
