---
layout: video
title: "zrepl - ZFS replication"
date: 2018-06-09
author: Christian Schwarz
email: me@cschwarz.com
youtube: c1LKeyP1mos
---
ZFS replication functionality has been greatly extended in recent years, e.g., through bookmarks and compressed, deduplicated and encrypted send & receive. However, the surrounding tooling has struggled to keep up: Many shell-script-based solutions are left unmaintained by their original authors. We present zrepl, a one-stop solution for continuous ZFS filesystem replication, featuring automatic snapshotting, replication and pruning of filesystem snapshots.

zrepl runs as a daemon and provides activity information via detailed structured logging, control & status commands and remote monitoring endpoints. Replication is implemented using a custom low-overhead RPC-protocol that only requires an authenticated, reliable, bidirectional byte stream channel. Explicit communication enables ZFS feature negotiation, cross-platform compatibility and the ability to distrust a remote zrepl instance, enabling SaaS-type use cases. The latter is particularly interesting in the light of upcoming OpenZFS native encryption. zrepl is implemented in Go and thus works on and between all combinations of OSes supporting OpenZFS.

This talk presents

* the core functionality provided by zrepl,
* typical use cases,
* software architecture and implementation,
* pain points / lacking functionality / feature wishlist in OpenZFS.

zrepl home page & docs: https://zrepl.github.io/

zrepl GitHub: https://github.com/zrepl/zrepl