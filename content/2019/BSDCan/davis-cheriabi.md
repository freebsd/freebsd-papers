---
layout: slides
title: "CheriABI: Hardware enforced memory safety for FreeBSD"
date: 2019-05-18
author: Brooks Davis
email: brooks.davis@sri.com
slides: 20190518-bsdcan-cheriabi.pdf
---
Memory safety bugs such as buffer overflows are an ongoing source of
security vulnerabilities. CheriABI is a new process model for FreeBSD
on the Capability Hardware Enhanced RISC Instructions (CHERI) hardware
platform which eliminates the vast majority of buffer overflows and
significantly increases the difficulty of control-flow attacks such
as return-oriented programming. Our protections cover programs, the C
run-time environment including the dynamic linker, and kernel access to
user memory. We have ported virtually all of the FreeBSD user space this
platform demonstrating that memory safety can be fitted to existing C
software.

**Further Reading**:
[CheriABI: Enforcing Valid Pointer Provenance and Minimizing Pointer Privilege in the POSIX C Run-time Environment (Conference paper)](https://www.cl.cam.ac.uk/research/security/ctsrd/pdfs/201904-asplos-cheriabi.pdf)
[CheriABI: Enforcing Valid Pointer Provenance and Minimizing Pointer Privilege in the POSIX C Run-time Environment (Extended technical report)](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-932.pdf)
