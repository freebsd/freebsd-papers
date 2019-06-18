---
layout: slides
title: "Netflix and FreeBSD: Reflections on Running FreeBSD Head in Production"
date: 2019-05-17
author: Jonathan Looney
youtube: veQwkG0WdN8
---
Netflix has built a CDN to distribute streaming media through most of the world. The content caches run a lightly customized version of the FreeBSD operating system's head branch. This presentation will describe Netflix's development process, and give some reflections on Netflix's experience using FreeBSD head in production.

Netflix has built a CDN, called Open Connect, to distribute streaming media through most of the world. According to Sandvine, Netflix accounts for approximately 15% of all downstream traffic volume across the entire internet. The content caches in the Netflix CDN, also known as Open Connect Appliances (or, simply, OCAs), run a lightly customized version of FreeBSD.

In some ways, this is nothing special: many products are based on an open-source operating system. However, Netflix does something slightly unusual, in that its OCA operating system code closely tracks the FreeBSD "head" branch (their development branch). In fact, a commit to the upstream FreeBSD development branch will usually be fully deployed across Netflix's CDN within 4-12 weeks.

Although it might seem scary to run "development" code in production, we find that it works very well in practice. The FreeBSD development branch is usually quite stable. Additionally, we expect that we will find some bugs. However, we find that it is much better to find and fix those sooner, rather than later. Also, Netflix is committed to upstreaming most of our customizations that have general applicability. Tracking the upstream development branch keeps us in the best position to easily upstream our changes.

In this presentation, Jonathan Looney will explain how Netflix uses the FreeBSD development branch code to help Netflix produce the robust operating system which supports the Netflix CDN. The presentation will describe Netflix's development process, and give some reflections on Netflix's experience using FreeBSD head in production.

Open Connect: https://openconnect.netflix.com/

Open Connect Appliance: https://openconnect.netflix.com/appliances/

SandVine: https://www.sandvine.com/phenomena