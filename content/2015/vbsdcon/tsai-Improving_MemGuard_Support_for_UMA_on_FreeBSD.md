---
layout: slides
title: "Improving MemGuard Support for UMA on FreeBSD"
date: 2015-09-13
author: Chang-Hsien Tsai (Luke)
email: luke.tw@gmail.com
youtube: Gd1rxMSLMYc
---
MemGuard can detect use-after-free kernel memory bugs on FreeBSD. It was originally designed to protect the memory allocated by malloc(9). Later the support for UMA was added. However, some UMA zones are not compatible with MemGuard. For example, some UMA zones use the conflict field in vm_page structure. Some zones have init and fini functions that need to be called. This results in panic whe MemGuard tries to guard these zones.

This talk will cover the implementation and experience of MemGuard. With this enhancement, three previous unknown memory bugs are found.
   [1] https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=197246
   [2] https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=199518
   [3] https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=199705

**Further Reading**: [FreeBSD Journal article](http://www.onlinedigeditions.com/publication/?i=279197&article_id=2307847&view=articleBrowser&ver=html5#{%22issue_id%22:279197,%22numpages%22:1,%22view%22:%22articleBrowser%22,%22article_id%22:%222307847%22})