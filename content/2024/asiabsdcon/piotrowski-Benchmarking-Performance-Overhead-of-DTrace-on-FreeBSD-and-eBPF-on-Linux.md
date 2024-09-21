---
layout: slides
title: "Benchmarking Performance Overhead of DTrace on FreeBSD and eBPF on Linux"
date: 2024-03-24
author: Mateusz Piotrowski
---

DTrace and eBPF are today’s most potent observ- ability tools available on
general-purpose operating systems. They empower users to ask random questions
and receive complex answers about any part of the system. Their performance is
unmatched by any traditional observability tools.

Unfortunately, their performance characteristics are not well- researched,
partially because designing a benchmark to measure the measurement tool is
challenging.

In this paper, we learn about the basics of art benchmarking and the importance
and difficulties of operating system instru- mentation. We review three
generations of observability tools to understand their design and
implementation limitations. Finally, we design, implement, and conduct a
microbenchmark and an application benchmark to peak into the enigmatic domain
of DTrace and eBPF performance overhead.
