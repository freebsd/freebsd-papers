---
layout: slides
title: "CheriABI: Hardware enforced memory safety for FreeBSD"
date: 2019-09-21
author: Brooks Davis
email: brooks@FreeBSD.org
youtube: cAuhWjDDM0k
---
Memory safety bugs such as buffer overflows are an ongoing source of security vulnerabilities. CheriABI is a new process model for FreeBSD on the Capability Hardware Enhanced RISC Instructions (CHERI) hardware platform which eliminates the vast majority of buffer overflows and significantly increases the difficulty of control-flow attacks such as return-oriented programming.

Our protections cover programs, the C run-time environment including the dynamic linker, and kernel access to user memory. We have ported virtually all of the FreeBSD user space this platform demonstrating that memory safety can be fitted to existing C software.

**Brooks Davis**

Brooks Davis is a Senior Software Engineer in the Computer Science Laboratory at SRI International and a Visiting Research Fellow at the University of Cambridge Computer Laboratory. He has been a FreeBSD user since 1994, a FreeBSD committer since 2001, and was a core team member from 2006 to 2012 and 2019 to present.

Brooks earned a Bachelors Degree in Computer Science from Harvey Mudd College in 1998. His computing interests include security, operating systems, networking, high performance computing, and, of course, finding ways to use FreeBSD in all these areas. When not computing, he enjoys cooking, brewing, gardening, woodworking, blacksmithing, and hiking.
