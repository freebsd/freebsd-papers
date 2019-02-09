---
layout: paper
title: "Continuous Integration of the FreeBSD Project"
date: 2016-09-25
author: Li-Wen Hsu
email: lwhsu@FreeBSD.org
---
FreeBSD's continuous integration project starts in the late 2013. We use
Jenkins automation server to build our continuous integration system. It
monitors the svn repository for new commits and triggers a new build of it. In
each build. The build server compiles the latest code and creates image to run
tests on it. In the meantime, we collect the compiler warnings and perform some
further checks like clang-scan build. All these information are published to
the developers and users to improve the quality of the FreeBSD project.

This talk will discuss about how we setup the FreeBSD continuous integration
system, future work.and how to participate.

Slides: https://docs.google.com/presentation/d/1xUFb5yaWUAeIaImb6CBdFiy92ccS8FW1k-02nmAktcE/pub
