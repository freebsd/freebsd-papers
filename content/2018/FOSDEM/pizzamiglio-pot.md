---
layout: slides
title: "pot: another container framework based on jails and ZFS"
date: 2018-02-03
author: Luca Pizzamiglio
email: pizzamig@freebsd.org
youtube: 8zIFhHIZDD8
---
## A personal/educational project to run containers with the power of FreeBSD

The initial idea of pot was to imitate containers, like docker, but using FreeBSD technologies, like jails and ZFS. The goal was to run several "pots" on my laptop to serve my needs and, at the same time, to learn how to manage them efficiently, especially in term disk usage. Instead of using/extending existing tools, like ezjail or iocage, I decided to reinvent the wheel and to write myself a new tool. After some time, I realized that making pot more generic and available to everyone could be a good idea and that's what I intend to present. I also show some interesting use cases and, hopefully, a live demo.
