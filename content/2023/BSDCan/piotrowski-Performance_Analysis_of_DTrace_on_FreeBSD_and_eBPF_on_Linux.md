---
layout: slides
title: "Measuring Performance Overhead of Tracing with DTrace and eBPF"
date: 2023-05-19
author: Mateusz Piotrowski
---
Tools such as DTrace and eBPF allow performance engineers to measure the
performance of almost any part of an operating system. These tools can be
easily hooked into arbitrary parts of the code base and gather the exact
statistics one needs. But then comes the question of the overhead. Even though
tracing tools are often advertised as having almost no overhead, they still
impose a penalty on the running system.

The presentation focuses on designing and conducting benchmarks to measure the
overhead of DTrace on FreeBSD and eBPF on Linux. We will compare some workloads
and analyze the performance hit that software takes when actively traced. The
goal is to gather intuitions on what overhead one can expect when tracing a
production system. Bonus points if we pinpoint a bottleneck or two.

It is a continuation of research presented in Vienna at EuroBSDCon 2022.
