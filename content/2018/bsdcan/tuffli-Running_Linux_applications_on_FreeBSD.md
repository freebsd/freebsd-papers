---
layout: slides
title: "Running Linux applications on FreeBSD"
date: 2018-06-09
author: Chuck Tuffli
email: chuck@freebsd.org
youtube: 9N3NrPeCJpk
---
While FreeBSD has been able to run Linux binaries for many years, the large ecosystem of Docker images leads to some interesting use cases for FreeBSD developers and users. This talk will review how the various kernel modules execute Linux binaries, several ways to use this functionality, and the work in progress to improve the Linux syscall compatibility.

FreeBSD has been able to run Linux binaries since 1995, not through virtualization or emulation, but by understanding the Linux executable format and providing a Linux specific system call table. Originally, this was for the noble goal of playing the video game, Doom. Over time, many Linux applications and libraries have been packaged and made available through the FreeBSD Ports Collection. But because FreeBSD tools do not understand Linux package dependencies, this process is manual and time consuming.

Docker has popularized the use of Linux Containers, similar to FreeBSD's jails, but more importantly, has lead to publishing a wide variety of both Linux system and application images. These images allow FreeBSD users to download a variety of Linux system images and use their native tools to provide applications not available through the Ports Collection.

This started as a simple quest to build Linux device drivers and applications on my FreeBSD system, but the journey has lead to an understanding of the inner workings of the Linux Binary Compatibility layer. It started by running applications from ports, progressed to chroot'd Docker image based environments, and has end up in Docker image based jails. The talk will cover the technology behind this capability as well as examples of using this in practice. Additionally, it will cover some of my work-in-progress to enhance the Linux support for network sockets, capabilities (a.k.a. privileges), mremap, and others.

Sample scripts to create and start Linux environment: https://gitlab.com/ctuffli/lxtools