---
layout: slides
title: "X11 and Wayland: A tale of two implementations"
date: 2020-02-02
author: Raichoo Ketchum
email: raichoo@acmelabs.space 
youtube: 8E0SOWo-Gsg
---
## Implementing the hikari window manager/compositor

In this talk I will outline my journey implementing my X11 window manager hikari and the corresponding Wayland compositor shortly after. hikari is a stacking window manager/compositor with some tiling capabilities. It is still more or less work in progress and currently targets FreeBSD only but will be ported to Linux and other operating systems supporting Wayland once it has reached some degree of stability and feature completeness.

This talk covers:

 * a brief explanation regarding differences between X and Wayland
 * some of hikari's design goals and motivation
 * choice of programming language
 * an overview of libraries that were used
 * tools for ensuring code quality and robustness
 * obstacles
 * resources that helped me to implement the whole thing

Slides hosted by author: https://acmelabs.space/~raichoo/fosdem/#1
