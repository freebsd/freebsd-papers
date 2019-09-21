---
layout: slides
title: "How SMPng Works and Why It Doesn't Work The Way You Think"
date: 2013-02-06
author: John Baldwin
email: jhb@FreeBSD.org
audiolink: https://www.nycbug.org/event/10327/nycbug-2013-02-06.mp3
venue: NYC*BUG
---
Modern x86 CPUs have hit a wall in frequency scaling and are now 
expanding sideways by adding more cores. Adding more cores does not 
magically multiply performance, however. John talks about some of the 
reasons that it doesn't.

In 2000, FreeBSD launched a project to multithread its kernel to more 
fully take advantage of modern SMP machines. This talk will give an 
overview of that project's history and continuing work on improving 
scalability.
