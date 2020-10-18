---
layout: video
title: "BSD Honeypots - Of course it runs on BSD"
date: 2020-06-06
author: Michael Shirk
youtube: qmq1GTJuxOw
---
In the past, there was some interest in the setting up of honeypots on BSD operating systems with tools like honeyd. Honeypots attempt to capture malicious code, network worms and attackers by emulating vulnerable services using a variety of methods. An opportunity came up for me to try to capture some malicious code using a simple setup with FreeBSD and jails. The setup was simple and easy to replicate as a way to perform security research on current attacks across the Internet and correlate with other threat sources for analysis.

The goal for this talk will be to walk through a brief introduction of honeypots, followed by a background of honeypots on the BSD operating systems such as honeyd. I will walk through the simple steps I used to setup the necessary services and network configs with a FreeBSD jail and the additional jails I utilized for monitoring the honeypot with a Network Security tool such as Zeek, Suricata or Snort. I will also cover some other ways to setup honeypots on all of the BSD operating systems.
