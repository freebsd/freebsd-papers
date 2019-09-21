---
layout: paper
title: Locking in the Multithreaded FreeBSD Kernel
date: 2002-02-13
author: John Baldwin
email: jhb@FreeBSD.org
---
About a year ago, the FreeBSD Project embarked on the ambitious task of multithreading its kernel. The primary goal of this project is to improve performance on multiprocessor (MP) systems by allowing concurrent access to the kernel while not drastically hurting performance on uniprocessor (UP) systems. As a result, the project has been dubbed the SMP next generation project, or SMPng for short.
Multithreading a BSD kernel is not just a one-time change; it changes the way that data integrity within the kernel is maintained. Thus, not only does the existing code need to be reworked, but new code must also use these different methods. The purpose of this paper is to aid kernel programmers in using these methods.
It is assumed that the audience is familiar with the data integrity methods used in the traditional BSD kernel. The paper will open with a brief overview of these traditional methods. Next, it will describe the synchronization primitives new to the multithreaded FreeBSD kernel including a set of guidelines concerning their use. Finally, the paper will describe the tools provided to assist developers in using these synchronization primitives properly. 
