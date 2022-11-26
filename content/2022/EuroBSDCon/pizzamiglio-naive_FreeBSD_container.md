---
layout: slides
title: "How far a naive FreeBSD container implementation can go"
date: 2022-09-18
author: Luca Pizzamiglio
youtube: b0IB0mc2KTE
---
### Success and failures for a project with good intentions		

In this talk, I'm going to present the current status of `pot`, a framework to
provide container-alike workflow on FreeBSD.

`pot` started in 2018 and it has been developed mainly in shell scripts (the
naive part of the title) to prove that FreeBSD is ready to support containers.

While speaking about the current status, I'll talk about the last 2 years
development, the challenges to make the framework "production ready" and what
is still missing.

I'll also present all the related projects, like Nomad support and Pothub, a
community driven public registry for `pot` images.

Additionally, I'm going to present some personal opinion about containers in
FreeBSD, based on my experience in the project.
