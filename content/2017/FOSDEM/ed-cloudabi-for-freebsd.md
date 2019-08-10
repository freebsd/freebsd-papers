---
layout: slides
title: "CloudABI for FreeBSD"
date: 2017-02-04
author: Ed Schouten
email: ed@freebsd.org
video: https://video.fosdem.org/2017/K.3.201/cloud_abi.mp4
---
## How does it work?

One of the fundamental problems with UNIX-like operating systems is that they don't seem to make it easy and intuitive to develop applications that are strongly hardened against exploits through sandboxing. With CloudABI, we're trying to make this process a lot easier, by having an environment that is purely based on capability-based security.

In another talk in the main track I'm going to give a more general talk about CloudABI, explaining what the mindset behind the project. During this talk in the BSD devroom I want to focus on one specific aspect, namely how FreeBSD's runtime environment for CloudABI works.

CloudABI is a simplified POSIX-like runtime environment that is inspired by FreeBSD's Capsicum. It allows you to create programs that can solely interact with the environment through file descriptors (capabilities). Compared to traditional UNIX-like systems, this approach has three advantages:

 1. It reduces the impact of exploits. If an attacker manages to take over control of a CloudABI application, it can only access those resources that the application was designed to use (for a networked service: typically an already bound TCP socket and some data directories). This is different from most traditional UNIX-like systems, where an attacker would gain access to all resources that the user running the application can access, which is very broad.
 2. It makes applications easier to test. By knowing that an application can only access those resources that are provided explicitly, the entire environment in which the application runs can be customized for testing.
 3. Similarly, it makes applications easier to deploy. This model tends to reduce the need for using containers and virtual machines. Applications can be started directly, while still providing the necessary isolation from the rest of the system.

 An interesting aspect of CloudABI is that it's cross-platform. You can compile a CloudABI program once and run exactly the same executable both on FreeBSD, macOS and Linux. In this talk I want to focus on this specifically: how is FreeBSD capable of running these programs? Topics I'll be covering during this talk include:

 * FreeBSD's image activator framework: the code that parses and loads executables.
 * The ELF file format
 * System calls and system call tables
 * vDSOs: Virtual Dynamic Shared Objects
