---
layout: paper
title: "Dirty deals: the story of a data corruption bug in OpenZFS"
date: 2024-03-23
author: Rob Norris
email: robn@despairlabs.com
venue: AsiaBSDCon 2024
---

In November 2023 a silent data corruption bug was discovered in the recently
released OpenZFS 2.2.0. The bug was reported, and quickly correlated by the
community with a new feature, “block cloning”, which even before its release
had gained a reputation for instability and data loss, to the point of being
disabled by default in FreeBSD 14. A 2.2.1 release was quickly put together,
disabling the feature.

One of OpenZFS’ key selling points is its ability to detect and correct all
kinds of data corruption, so news of its apparent failure quickly spread
through tech news and social media, aided by its somewhat prickly relationship
with some other parts of the open-source software world. This naturally led to
a lot of confusion and concern from home and business OpenZFS users alike,
worried about the integrity of their data.

With many outside eyes on the bug report, a reproduction test case was
developed and it was quickly shown that the bug was present on the previous 2.1
series, and it was theorised that it might have been present right back to the
original open-source ZFS release. This naturally caused even more confusion and
concern, as now people were concerned about the integrity of their decades-old
archive storage.

Over the Thanksgiving long weekend a few OpenZFS developers and many users
rallied around the problem. A workaround was identified and documented. The bug
was studied and gradually understood, and a fix was developed. People shared
ideas and how might identify if their data was corrupt. Others theorised about
different workloads that could make the problem easier or harder to hit. Still
others took it upon themselves to find ways to run older versions, to find out
just how far back the problem went.

This is a story about a 15-year old bug, where it came from, how it works, how
it eluded users and developers alike through that time, and how a community
pulled together to understand and fix it.
