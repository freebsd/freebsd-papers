---
layout: paper
title: "CheriABI: Enforcing Valid Pointer Provenance and Minimizing Pointer Privilege in the POSIX C Run-time Environment"
date: 2019-04-14
author: Brooks Davis
email: brooks.davis@sri.com
paper: 201904-asplos-cheriabi.pdf
slides: 20190414-cheriabi.pdf
---
**Authors:** Brooks Davis, Robert N. M. Watson, Alexander Richardson, Peter G. Neumann, Simon W. Moore, John Baldwin, David Chisnall, James Clarke, Nathaniel Wesley Filardo, Khilan Gudka, Alexandre Joannou, Ben Laurie, A. Theodore Markettos, J. Edward Maste, Alfredo Mazzinghi, Edward Napierala, Robert Norton, Michael Roe, Peter Sewell, Stacey Son, Jonathan Woodruff

**Abstract**: The CHERI architecture allows pointers to be implemented as capabilities
(rather than integer virtual addresses) in a manner that is compatible
with, and strengthens, the semantics of the C language.  In addition to
the spatial protections offered by conventional fat pointers, CHERI
capabilities offer strong integrity, enforced provenance validity, and
access monotonicity.  The stronger guarantees of these architectural
capabilities must be reconciled with the real-world behavior of
operating systems, run-time environments, and applications.  When the
process model, user-kernel interactions, dynamic linking, and memory
management are all considered, we observe that simple derivation of
architectural capabilities is insufficient to describe appropriate
access to memory.  We bridge this conceptual gap with a notional
abstract capability that describes the accesses that should be allowed
at a given point in execution, whether in the kernel or userspace.  To
investigate this notion at scale, we describe the first adaptation of a
full C-language operating system (FreeBSD) with an enterprise database
(PostgreSQL) for complete spatial and referential memory safety.  We
show that awareness of abstract capabilities, coupled with CHERI
architectural capabilities, can provide more complete protection, strong
compatibility, and acceptable performance overhead compared with the
pre-CHERI baseline and software-only approaches.  Our observations also
have potentially significant implications for other mitigation
techniques.

**Further Reading**: [Extended technical report version](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-932.pdf)
