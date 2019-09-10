---
layout: video
title: "The Realities of DTrace on FreeBSD"
date: 2017-09-09
author: George Neville-Neil
email: gnn@neville-neil.com
youtube: 0ke7p_Mh6Mg
---
For more than a year we have been using DTrace as one of the three core components of a security research project, CADETS. Unlike earlier users of DTrace, which were focused on occasional, deep debugging sessions, the CADETS project uses DTrace to bring total system transparency to both the operating system and the applications that are running on top of it. The use of "always-on tracing" pushes the DTrace system up to, and often, past its limits and shows how some of the original design tradeoffs need to be revisited to address the needs of our project. Our talk covers our current efforts to extend and improve the DTrace framework in FreeBSD, including performance and programming improvements to address the needs of always-on tracing as well as integration with FreeBSD's audit subsystem and the addition of machine-readable output for use by creators of downstream security-analysis tools. 