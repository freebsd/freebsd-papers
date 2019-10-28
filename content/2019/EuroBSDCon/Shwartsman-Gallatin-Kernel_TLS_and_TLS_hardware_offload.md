---
layout: slides
title: "Kernel TLS and TLS hardware offload"
date: 2019-09-22
author: Slava Shwartsman, Drew Gallatin
---
TLS (Transport Layer Security) is a widely-deployed network protocol used for providing cryptographically proven security and authentication of TCP sessions. A kernel implementation of TLS will provide access to TLS hardware offload, ability to access unencrypted bytes of data in the kernel, and a reduction in copies to and from userspace by allowing the use of the sendfile(9) system call for TLS encrypted data.

This talk will start from explaining the basics of TLS protocol, using OpenSSL as an example, cover the advantages and motivation for kernel TLS (KTLS) and later will dive in to the implementation.

One of the major advantages of KTLS is the ability to offload TLS symmetric crypto processing to the network device. This talk will cover TLS hardware offload approaches, like TOE and inline TLS acceleration.

We will close with some performance numbers comparing OpenSSL, KTLS and hardware offloaded TLS with data taken from Netflix servers.
