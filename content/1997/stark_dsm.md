---
layout: paper
title: A Distributed Shared Memory Facility for FreeBSD
date: 1997-01-01
author: Eugene Stark
email: stark@freebsd.org
paper: /_assets/usenix1997_stark_dsm.pdf
---
This paper describes the design and implementation of a distributed shared memory facility we have implemented for the FreeBSD operating system (a descendant of 4.4BSD that runs on the PC architecture). Interesting aspects of the design are: (1) the consistency protocol uses unreliable datagram communication, but is robust with respect to message loss, and in the normal case requires only two datagrams to handle a read fault; (2) the facility provides a simple programming interface that does not require any socket or network programming to use; (3) the facility extends the FreeBSD VM system in a very non-intrusive way. 
