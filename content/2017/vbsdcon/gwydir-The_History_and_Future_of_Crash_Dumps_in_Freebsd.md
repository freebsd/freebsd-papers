---
layout: slides
title: "The History and Future of Crash Dumps in FreeBSD"
date: 2017-09-09
author: Sam W. Gwydir
youtube: iqnyFp3rhlY
---
Crash dumps, also known as core dumps, have been a part of BSD since its beginnings in Research UNIX. Though 38 years have passed since doadump() came about in UNIX/32V, core dumps are still needed and utilized in much the same way they were then. However, as underlying assumptions about the ratio of swap to RAM have proven inappropriate for modern systems, several extensions have been made by those who needed core dumps on very large servers, or very small embedded systems.

We begins with a background on what core dumps are and why operators might need them. Then several timelines are used to characterize the changing nature of the core dump procedure in FreeBSD, with the side effect of providing a history of archtecture support from UNIX v6 through to FreeBSD 12. Following that the current state of the core dump facility and some of the more common extensions in use are examined.

We conclude with my experience porting Illumos' ability to dump to swap on a ZFS zvol to FreeBSD and what that provides the operator.

In addition a complete history of core dumps in UNIX and BSD was produced as research for this paper and can be found in the appendix.