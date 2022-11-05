---
layout: video
title: "Making FreeBSD QUIC"
date: 2022-09-18
author: Tom Jones
youtube: MOtsTyp9LZk
---
The Internet has continued to evolve throughout its life and with these changes
the protocols we use to move information around have had to adapt to keep up.
TCP, the work horse of the Internet has reliably been delivering bytes for many
decades, but the protocol lacks room to grow to meet future challenges.

QUIC was created as a new protocol to enable future evolution in how we move
bits around the Internet. QUIC adds always Authentication and Encryption,
features that allow much improved congestion control, better features for CDN
operators and higher reliability for end users.

Once QUIC escaped into the IETF it followed an open development process, but
other than Mac OS laptops for development, QUIC was mostly designed and tested
on Linux systems.

With this Linux focus we have to wonder if BSD platforms are being left behind?

This talk looks at the performance of QUIC implementations on Linux and FreeBSD
and explores the changes that made QUIC implementations faster.  We will will
dig into network performance and techniques that can used to understand the
performance of any application on FreeBSD.

With this we try to answer the question, How can we make FreeBSD QUIC?
