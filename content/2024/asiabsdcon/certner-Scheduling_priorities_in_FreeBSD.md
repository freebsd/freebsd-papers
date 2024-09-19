---
layout: paper
title: "rtprio(2) and POSIX(.1b) priorities, and their
FreeBSD implementation: A deep dive (and sweep)"
date: 2024-03-22
author: Olivier Certner
email: olce@FreeBSD.org
venue: AsiaBSDCon 2024
---

Although UNIX’s descendants or derivatives are not hard real-time operating
systems, some have support for soft real-time through allowing to assign to
userland processes higher priorities normally reserved to the system, sometimes
coupled with preemption of kernel tasks, making them suitable as a fundation of
soft real-time system. POSIX standardized its first real-time extensions in 1993
in a document usually referred to as POSIX.1b. At that time, however, some
operating systems already had support for soft real-time in the form of ad-hoc
APIs, such as System V Release 4 (SVR4) with its priocntl(2) system call and
HP/UX with its rtprio(2) one. FreeBSD first adopted its own rtprio(2) system
call in 1994, largely based on HP/UX’s with extensions such as idle processes.
POSIX.1b extensions concerning processes were implemented later, in 1998, and
some preliminary thread support added the next year. Since then, these APIs have
been present in the system for applications to use.

In this paper, we provide a thorough description of both FreeBSD’s rtprio(2) and
POSIX.1b’s scheduling interfaces and embark on a journey around FreeBSD’s
implementation of scheduling priorities. It started with a desire to fix a few
apparently simple bugs of rtprio(2) and to add some reasonable features and, one
thing leading to another, became an almost complete rewrite of this system call
and the POSIX.1b’s interfaces’ implementations. We will expose the many problems
that the current implementation has, in terms of POSIX compliance, security and
consistency and how we are fixing them. As of this writing, this project is
still a work in progress, and we will report about its status during the
conference presentation.
