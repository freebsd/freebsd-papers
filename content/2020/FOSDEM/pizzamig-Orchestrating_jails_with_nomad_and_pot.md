---
layout: slides
title: "Orchestrating jails with nomad and pot"
date: 2020-02-02
author: Luca Pizzamiglio
email: pizzamig@FreeBSD.org
video: https://video.fosdem.org/2020/AW1.121/orchestrating_jails.webm
---
## A container-based cloud computing platform for FreeBSD

Docker and Kubernetes are changing the way to deploy services and applications
in the Linux world. What about FreeBSD? 2 years ago we presented pot, another
jail abstraction framework. In time, the pot framework has developed to provide
features containers-alike. The plugin interface provided by nomad (a container
orchestrator), allowed us to develop a driver for pot, enabling nomad to
orchestrate pot jails. In this talk, we'd like to present this FreeBSD-based
ambitious alternative to Docker-Kubernetes
