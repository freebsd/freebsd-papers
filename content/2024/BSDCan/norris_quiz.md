---
layout: video
title: "quiz: tiny VMs for kernel development"
date: 2024-06-01
author: Rob Norris
email: robn@despairlabs.com
venue: BSDCan 2024
youtube: w_tC-D6xWIk
---

At the start of 2023 I traded my 20-year career as a Linux sysadmin for a new
life as a full time OpenZFS developer. Going great, thanks for asking!

Because fast iterative development sucks when you need to wait for a reboot
after every kernel panic, I wrote quiz, a tool to make fast edit-compile-test
cycles on kernel code possible. Under the hood it uses QEMU’s “microvm” profile
and a custom kernel config to boot from cold into the OpenZFS test suite in a
couple of seconds. Its great, and I use it hundreds of times a day.

My FreeBSD-using colleagues naturally said “cool, but what about us?!” so I
started looking at what it would take bring quiz to FreeBSD. The answer to that
is “its complicated”, and involves either adding bhyve to QEMU as a hardware
virtualisation backend, or adding support for direct kernel loading support to
/usr/sbin/bhyve. “Why not both?” I said, before promptly shriveling into a corn
cob.

This talk will show you quiz in action, present the Linux direct boot sequence
and show how I taught bhyve about it, also show how QEMU would like to work and
why it doesn’t quite line up with bhyve’s view of the world, and hopefully show
you how low-level kernel hacking for any OS can be made as simple as hacking on
any other program.
