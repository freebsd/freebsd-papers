---
layout: video
title: "Why fsync() on OpenZFS can’t fail, and what happens when it does"
date: 2024-05-31
author: Rob Norris
email: robn@despairlabs.com
venue: BSDCan 2024
youtube: dfH0I6D9ZAA
---

On OpenZFS, fsync() cannot fail - it will wait until the application’s changes
are on disk before it returns. If there is a problem, such as a hardware
failure, that causes the pool to suspend, then it will block until the pool
returns. This could be seconds, hours, or never, depending on the nature on the
failure.

Modern distributed systems can often cope with this type of failure by
redirecting requests to another node, but they can only do this if fsync()
returns an error instead of blocking.

In this talk I describe how OpenZFS implements fsync() and why it blocks when
the pool fails. I then discuss a series of changes made to make it possible for
fsync() to return failure - and what it means for applications when it does.
