---
layout: video
title: "LWPMFS: Light-Weight Persistent Memory Filesystem"
date: 2018-10-18
author: Ravi Pokala
email: rpokala@freebsd.org
youtube: YOhPBEqoiek
paper: 2018-10-18-MeetBSD-DevSummit-LWPMFS.pdf
venue: MeetBSD Developer Summit, Intel Santa Clara
---
Panasas creates high-capacity, high-performance, high-availability storage
appliances. A perennial problem in storage is the tradeoff between
performance, which requires aggressive cacheing, and data safety, which
requires getting the data onto stable storage as soon as possible. In this
context "stable" includes "persistent across power failure".

The first part of this talk recaps how Panasas originally addressed
power-failure safety: an enclosure-wide battery backup, part of our custom
hardware and software platform.

The second part of this talk describes how Panasas is addressing
power-failure safety in the world of Commercial Off-The-Shelf (COTS)
hardware platforms: an NVDIMM, drivers to interface with it, and a
persistent-memory-aware filesystem.
