---
layout: slides
title: "Title"
date: 2013-05-17 
author: Ivan Voras
email: ivoras@freebsd.org
paper: voras-benchmarking-freebsd.pdf
venue: Ottawa, Canada
---
This document summarizes Ivan Voras' plans to benchmark FreeBSD against Linux.
Some key points:

- The last major FreeBSD vs Linux benchmark was done in 2008, so an updated comparison is needed.
- Benchmarks will help identify areas for FreeBSD improvement.
- Tests will be run on identical hardware configurations to allow for accurate comparisons.
- Software tested includes FreeBSD 9.1, 10, CentOS 6.3 and various applications.
- Benchmarks like Blogbench and PostgreSQL show some areas where FreeBSD could see better performance, like reducing lock contention between concurrent operations.
- Results will help developers prioritize optimization work and provide data for administrators to evaluate the operating systems. 
