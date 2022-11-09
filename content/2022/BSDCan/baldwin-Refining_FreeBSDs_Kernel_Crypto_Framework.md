---
layout: slides
title: "Refining FreeBSD's Kernel Crypto Framework"
date: 2022-06-04
author: John Baldwin
youtube: OxnrUwtVZ0U
---
FreeBSD imported a modified version of the OpenCrypto Framework from OpenBSD nearly 20 years ago. At the time the primary use case was IPsec. Since then, new use cases have arisen including disk encryption and kernel-assisted TLS.

Over the past few years, several changes have been made to the framework to streamline the interfaces for both drivers and consumers. The new interface better supports newer cipher suites (in particular AEAD cipher suites). This talk will discuss these changes in detail.
