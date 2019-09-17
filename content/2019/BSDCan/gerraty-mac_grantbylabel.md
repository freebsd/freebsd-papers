---
layout: slides
title: "mac_grantbylabel: Securely controlled privilege escalations via maclabel"
date: 2019-05-18
author: Simon Gerraty
email:  sjg@juniper.net
---
When I joined Juniper in 2000, running daemons as non-root was on the todo list. With the recent move to basing Junos on FreeBSD 10 and later, we can finally do this by leveraging the MAC framework

Building Junos on FreeBSD stable/10 and later, we have the MAC framework to play with. We re-implemented Verified Exec as a mac module and the latest version allows us to associate a maclabel with a process.

Junos daemons need to perform a range of privileged operations, but the bulk of what they do could just as well be done as nobody.

This talk covers a new mac module - mac_grantbylabel which takes advantage of mac_priv_grant() and the labels set via mac_veriexec to allow for focused privilege escalations.

The end result is daemons can do their job with no code change, and only about 5% of the privileges they have running as uid 0.

Even if such a daemon were to be victim to a buffer overflow etc exploit, any exec would cause loss of all privileges.