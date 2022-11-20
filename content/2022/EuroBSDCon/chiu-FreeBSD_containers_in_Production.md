---
layout: slides
title: "FreeBSD containers in production. A NSFW guide."
date: 2022-09-18
author: Yan Ka Chiu
youtube: zN7BRJIm5NY
---
An overview and summarization of running FreeBSD containers on the cloud in
production.	

Two years ago, I joined a company to design and implement the entire backend
stack, in which we eventually chose to use FreeBSD to run a number of our
backend services, packaged as containers, alongside other services running on
Kubernetes.

This talk will explain the decision's rationale and summarize the good, the
bad, and the ugly of running FreeBSD containers on the cloud. I will also
demonstrate the tools we (ab)used to create, orchestrate and distribute these
services, evaluate the impact on DevOps and other aspects, and contrast them
with the Linux counterparts. Last but not least, we will try to conclude if
this is for everyone.
