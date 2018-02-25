---
layout: paper
title: GELIBoot
date: 2016-03-13
author: Allan Jude
email: allanjude@freebsd.org
---
With the growing popularity of ZFS Boot Environments, a solution was needed that allowed the kernel and loader to remain part of the primary filesystem, even if it was encrypted.
This paper provides an overview of the design of the GELI enabled boot code and loader, as well as the numerous challenges encountered during their development.
