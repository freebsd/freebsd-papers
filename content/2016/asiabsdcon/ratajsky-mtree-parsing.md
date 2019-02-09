---
layout: paper
title: "tree parsing and manipulation library"
date: 2016-03-12
author: Michal Ratajsky
email: michal.ratajsky@gmail.com
youtube: dvcHfbLd6gU
---
FreeBSD includes several programs which create or consume file system hierarchy descriptions in the mtree(5) format. These descriptions, also called specifications, have a broad range of uses, from automatically creating directory structures to security auditing. Each of the programs, namely mtree(8), bsdtar(1), install(1) and makefs(8), has its own implementation of the mtree format. This not only adds maintenance overhead, but also makes interoperability difficult, as each of the implementations only supports a limited subset of the format. In 2015, the libmtree library was created as part of the Google Summer of Code program to replace and unify the existing implementations.
