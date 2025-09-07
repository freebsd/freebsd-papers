---
layout: slides
title: "ZFS Direct IO Benchmarking Pitfalls"
date: 2025-06-13
author: Mateusz Piotrowski
youtube: tYCN8Yg-0JQ
---

Not too long ago, support for direct IO landed in OpenZFS after years of
discussions and reviews. We truly live in the future where we can finally
reject complicated caching and fully embrace the unbuffered conversations with
our disks. Or can we really?

Those of you who know a bit about ZFS know that the ARC is actually pretty
important (without one ZFS would historically stand for zzz 😴 instead of
Zetta). How could it be then that skipping the ARC might improve performance?

During the presentation we will discuss what workloads and setups benefit from
direct IO, what its limitations are, and what pitfalls to avoid during
benchmarking. We will also look at the implementation to understand how all the
promises of stability and compatibility were kept.

Direct IO is reported to deliver amazing performance boosts in some
deployments. Understanding how not to hold it wrong is a great first step to
potentially unlocking that speed-up on your systems too!
