---
layout: paper
title: GELIBoot
date: 2016-03-10
author: Allan Jude
email: allanjude@freebsd.org
slides: /_assets/AllanJude_GELIBoot_slides.pdf
paper: /_assets/AllanJude_GELIBoot_paper.pdf
---
With the growing popularity of ZFS Boot Environments, a solution was needed that allowed the kernel and loader to remain part of the primary filesystem, even if it was encrypted.
This paper provides an overview of the design of the GELI enabled boot code and loader, as well as the numerous challenges encountered during their development.
