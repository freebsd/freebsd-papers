---
layout: slides
title: "In-kernel TLS Framing and Encryption for FreeBSD"
date: 2020-06-05
author: John Baldwin
---
In the past year, several changes have been committed to FreeBSD to add support for in-kernel TLS framing and encryption on TCP sockets.

This talk will discuss the motivation for these changes as well as give an overview of the implementation. Compared to my earlier talk at vBSDCon, this talk will include details on recent changes to add support for receive offload and other changes I anticipate having made at the time of the talk.
