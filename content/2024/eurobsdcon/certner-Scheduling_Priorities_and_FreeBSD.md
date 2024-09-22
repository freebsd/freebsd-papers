---
layout: slides
title: "Scheduling Priorities and FreeBSD: A deep dive (and sweep)"
date: 2024-09-21
author: Olivier Certner
email: olce@FreeBSD.org
venue: EuroBSDCon 2024
---

In this talk, we will review FreeBSD’s rtprio(2) and POSIX.1b’s scheduling
interfaces and embark on a journey around FreeBSD’s implementation of scheduling
priorities. It started with a desire to fix a few apparently simple bugs of
rtprio(2) and to add some reasonable features and, one thing leading to another,
became an almost complete rewrite of this system call and the POSIX.1b’s
interfaces’ implementations, as well as some aspect of the schedulers. We will
touch on the most interesting problems that the implementation had, in terms of
POSIX compliance, security and consistency, and then explain how we fixed or are
fixing them. As of this writing, this project is still a work in progress, with
about ~30% of the changes being under review. We will report about its status
during the talk.
