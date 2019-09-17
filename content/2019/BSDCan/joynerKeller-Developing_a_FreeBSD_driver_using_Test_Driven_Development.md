---
layout: video
title: "Developing a FreeBSD driver using Test Driven Development: Could we develop a more maintainable driver with fewer bugs?"
date: 2019-05-17
author: Eric Joyner and Jacob Keller
youtube: 1pwVbpijcas
---
We needed to create a new driver for a new product, but we wanted to develop it in a way that reduced the number of bugs and would keep the code base maintainable in the future. We tried Test Driven Development.

Testing a network driver on real hardware is painful: bugs can result in essential subsystems behaving strangely or causing the kernel to panic; and regardless of the presence of bugs, physical hardware needs to spend time being configured, rebooting, or sending/receiving network traffic.

With the number and complexity of projects our team was tasked with increasing, we needed to find a way to reduce the amount of time spent fixing bugs or verifying that features work. So, we turned to the TDD (test-driven development) methodology which promises that more bugs can be discovered and fixed before they make it to testers (and users) while improving code maintainability.

This talk focuses on how we made the CppUTest framework work with and compile our FreeBSD driver code, other frameworks and utilites we needed, the problems we encountered trying to get kernel source code to compile in C++ and run in userspace, and future plans and areas that we want to investigate with TDD.

The test framework we used: https://cpputest.github.io/
