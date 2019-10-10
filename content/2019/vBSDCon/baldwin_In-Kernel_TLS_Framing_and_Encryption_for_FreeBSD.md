---
layout: slides
title: "In-Kernel TLS Framing and Encryp6on for FreeBSD"
date: 2019-09-06
author: John Baldwin
email: jhb@FreeBSD.org
youtube: la-ljVavd3c
venue: vBSDCon 2019
---
The sendfile(2) system call provides an efficient, zero-copy mechanism
for transferring large amounts of static content to remote clients
over a network socket.  It is particularly well suited to fulfilling
replies to FTP and HTTP requests.  When encryption is added to HTTP via
TLS, this efficiency is lost in current FreeBSD systems.  For several
years, Netflix has worked on a long-running project to enable the
efficiency and performance of sendfile(2) when using TLS for
HTTP.  This talk will describe the motivation for performing TLS
framing and encryption in the kernel and describe the current
implementation.  It will also provide a brief history of how the
implementation has evolved over time to support TLS offload in network
interface cards.

