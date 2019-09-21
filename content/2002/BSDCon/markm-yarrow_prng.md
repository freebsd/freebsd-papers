---
layout: paper
title: An implementation of the Yarrow PRNG for FreeBSD
date: 2002-02-13
author: Mark Murray
email: markm@freebsd.org
---
Computers are by their definition predictable. The problem of obtaining good-quality random numbers is well known.
There is a great need for entropy in the running kernel, as well as in user-space. The kernel needs to randomise TCP sequences, seed keys for IPSec, randomise PIDs, and so on. Starvation of these random numbers is a critical problem. Users need random keys, random filenames, nondeterministic games, random numbers for Monte-Carlo simulation and so on.
Kelsey, Schneier and Ferguson proposed an improved algorithm for providing statistically random numbers, at the same time cryptographically protecting their sequence and state. This is the Yarrow algorithm.
This work presents an implementation of this algorithm as the entropy device (/dev/random) in FreeBSD's kernel. 
