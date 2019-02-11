---
layout: slides
title: "Go based content filtering software on FreeBSD"
date: 2015-03-14
author: Ganbold Tsagaankhuu
email: ganbold@freebsd.org
---
Go is a new programming language compared to many other programming languages 
like C, C++, Java, etc., but it has many practical and useful features and 
in most cases more productive. On the other hand, FreeBSD has been around 
for very long time and proven to be the most reliable, one of the most 
powerful operating system available today. In this paper, we will discuss 
the issues, pros, cons, and common pitfalls of developing software in Go 
on FreeBSD and we chose content filtering software for this purpose, and 
called our project Shuultuur. First, we will describe a rational behind 
our choices for setting up our development environment and toolchain. 
In addition, we will list specific hurdles, that we faced, related to 
content filtering software, Go and FreeBSD. Furthermore, our real world 
benchmarking results in contrast to Dansguardian and other findings 
will be presented. Finally, we will conclude and discuss possible future works.
