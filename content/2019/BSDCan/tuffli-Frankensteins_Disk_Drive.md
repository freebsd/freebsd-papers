---
layout: slides
title: "Frankenstein’s Disk Drive"
date: 2019-05-18
author: Chuck Tuffli
email: chuck@freebsd.org
youtube: q4vtp4hJfao
---
Emulated devices in FreeBSD's bhyve hypervisor exist to provide compatibility with older operating systems. But with a few small changes, we can take a Dr. Frankenstein approach and allow the user to dynamically modify their behavior to create something new and beautiful.

Just kidding, the resulting havoc this wreaks on the guest operating system will bring out the villagers with their torches and pitchforks. This talk describes why you would want to do this and an implementation using the NVMe emulation.

There is a programmer's adage that says untested code will not work entirely the way you expect. But how do you test code which handles hardware errors? This presupposes having hardware that misbehaves in predictable and repeatable ways. Since this sort of unicorn does not exist, programmers will often create error injection hooks in the code. But this approach is problematic as the hooks tend to be static, work at cross-purposes with the actual code, and do not have access to user-space libraries and scripting languages that can help simplify the task.

FreeBSD's bhyve hypervisor and its emulated devices offers an alternative approach. To the guest software (a.k.a. the operating system), these appear to be actual hardware when in reality, they are small user-space programs. By adding hooks to the device emulation code, we can allow user defined plug-in's to modify the device behavior and allow better testing of device drivers and the code which relies on them. This talk will describe an experimental plug-in framework for bhyve's NVMe device emulation, example scripts, and the havoc that they can cause.