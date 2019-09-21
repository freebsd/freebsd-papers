---
layout: slides
title: "Crypto Acceleration on FreeBSD"
date: 2009-05-08
author: Philip Paeps
email: philip@
paper: philip-crypto_acceleration_on_freebsd.pdf
---
s more and more services on the internet become cryptographically secured, the load of cryptography on systems becomes heavier and heavier. Crypto acceleration hardware is available in different forms for different workloads. Embedded communications processors from VIA and AMD have limited acceleration facilities in silicon and various manufacturers build hardware for accelerating secure web traffic and IPSEC VPN tunnels.

This talk gives an overview of FreeBSD's crypto framework in the kernel and how it can be used together with OpenSSL to leverage acceleration hardware. Some numbers will be presented to demonstrate how acceleration can improve performance - and how it can curiously bring a system to a grinding halt.
