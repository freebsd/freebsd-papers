---
layout: paper
title: "FreeBSD Test Cluster Automation"
date: 2016-03-12
author: Kamil Czekirda
email: kczekirda@freebsd.org
youtube: FXE9zMVmU1o
---
"FreeBSD Test Cluster Automation" is a Google Summer of Code 2015 project for FreeBSD organization to create an infrastructure for automated tests building, installing and first booting process of FreeBSD. The base of this project is iPXE - Open Source Boot Firmware, which is used for controlling nodes. A small webapplication written in python is a frontend for the database where information about nodes, current states and states of revisions are saved. The project is also using mfsBSD and bsdinstall extension for an automatic and non-interactive installation process, it was done during Google Summer of Code 2014. On the server side the main part of the project is FreeNAS, it is used to provide shared storage and jails for applications. The ZFS filesystem with deduplication enabled on dataset for source code allows to save every tested revision of the source code with space saving. The scope of the project was only infrastructure, without focusing on tests. During the project simple tests of building and installing FreeBSD were made, it's similar to https://jenkins.freebsd.org/ but on the bare metal infrustructure and it's possible to test all commits, not all commits from one period of time like in jenkins. Another interesting application for this project is testing drivers, for example network card drivers. Inside testing cluster it's possible to build a driver after any commit, test it, measure and report.
