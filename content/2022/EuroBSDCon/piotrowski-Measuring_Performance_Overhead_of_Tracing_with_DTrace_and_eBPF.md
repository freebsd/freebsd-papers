---
layout: slides
title: "Measuring Performance Overhead of Tracing with DTrace and eBPF"
date: 2022-09-17
author: Mateusz Piotrowski
---
Tools such as DTrace and eBPF allow performance engineers to measure the
performance of almost any part of an operating system. These tools can be
easily hooked into an arbitrary part of the code base and gather the exact
statistics one needs. But then comes the question of the overhead. Even though
tracing tools are often advertised as having almost no overhead, they still
impose a penalty on the running system.

The presentation focuses on designing and conducting benchmarks in order to
measure the overhead of DTrace on FreeBSD and eBPF on Linux. We will compare a
number of workloads and analyze the performance hit, which an operating system
takes when being actively traced. The goal of the presentation is to see what
kind of overhead one can expect when tracing a production system.
