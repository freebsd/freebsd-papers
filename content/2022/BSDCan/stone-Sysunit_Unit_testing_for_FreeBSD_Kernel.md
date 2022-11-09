---
layout: video
title: "Sysunit: Unit Testing for the FreeBSD Kernel"
date: 2022-06-04
author: Ryan Stone
youtube: BVbJ9JDc18c
---
Introducing Sysunit, a unit testing framework for the FreeBSD kernel. Sysunit allows small pieces of kernel code to be run and tested entirely in userland. This significantly shortens the testing cycle and opens up opportunities to write tests for scenarios that are very difficult to induce on a running kernel.

This talk will introduce the basics of unit testing and how Sysunit adapts them to the FreeBSD kernel, discuss how unit testing can complement FreeBSD's testing strategy, and then walk developers through the process of writing and executing their own Sysunit tests.
