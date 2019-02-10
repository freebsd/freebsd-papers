---
layout: slides
title: "Implementing ZSTD in OpenZFS on FreeBSD"
date: 2018-06-09
author: Allan Jude
email: allanjude@freebsd.org
youtube: 7N6lMi6g5UU
---
The story of my journey through time and code to implementing ZSTD compression in OpenZFS on FreeBSD. Follow a novice developer through the initial naive attempt to add support for a new compression algorithm to ZFS, then through successive improvements and new stumbling blocks to ultimately arrive at a finished product.

* What is ZSTD, and why might I want to use it
* First attempt
* Allocating memory in the kernel is harder than it looks
* Ohh, you have to free that memory when you are finished it it..., what a scam
* The first prototype
* Alignment is a thing
* C is hard
* First working prototype
* Matt Ahrens pokes holes in your dreams
* Don't steal from future generations of ZFS
* You forgot about the L2ARC
* Getting it committed
* Conclusions
