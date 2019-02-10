---
layout: paper
title: Jails: Confining the omnipotent root
date: 2002-05-03
author: [ "Poul-Henning Kamp", "Robert N. M. Watson" ]
email: [ "phk@FreeBSD.org", "rwatson@FreeBSD.org"]
---
The traditional UNIX security model is simple but inexpressive.
Adding fine-grained access control improves the expressiveness, but
often dramatically increases both the cost of system management and
implementation complexity. In environments with a more complex
management model, with delegation of some management functions to
parties under varying degrees of trust, the base UNIX model and most
natural extensions are inappropriate at best. Where multiple mutually
untrusting parties are introduced, ‘‘inappropriate’’ rapidly
transitions to ‘‘nightmarish’’, especially with regards to data
integrity and privacy protection.
The FreeBSD ‘‘Jail’’ facility provides the ability to partition the
operating system environment, while maintaining the simplicity of
the UNIX ‘‘root’’ model. In Jail, users with privilege find that
the scope of their requests is limited to the jail, allowing system
administrators to delegate management capabilities for each virtual
machine environment.  Creating virtual machines in this manner has
many potential uses; the most popular thus far has been for providing
virtual machine services in Internet Service Provider environments.
