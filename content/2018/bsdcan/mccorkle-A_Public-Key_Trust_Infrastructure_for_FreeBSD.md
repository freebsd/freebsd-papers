---
layout: paper
title: "A Public-Key Trust Infrastructure for FreeBSD"
date: 2019-06-08
author: Eric McCorkle
youtube: DYHhTT05_7E
paper: mccorkle-A_Public-Key_Trust_Infrastructure_for_FreeBSD-paper.pdf
---
This talk describes a proposed design for a public-key trust infrastructure for the FreeBSD operating system which manages the notion of delegated trust in the form of public-key cryptographic signatures. It is designed to integrate easily with existing userland applications as well as other similar components such as secure/trusted boot and the NetBSD VeriExec infrastructures, and to provide a workable foundation for future developments. Additionally, it is designed in such a way that existing post-quantum signature schemes can be used practically.

This talk gives a detailed overview of a proposed design for a public-key trust infrastructure for the FreeBSD operating system. This proposal has been developed in response to discussions in various venues, including the FreeBSD mailing lists as well as plenary sessions at previous BSD conferences. It aims to design, develop, and ultimately deploy a powerful and general trust infrastructure that will hopefully become the foundation for new developments in operating system security and provide FreeBSD and the rest of the BSD family with new tools for growth. This infrastructure has a number of potential uses, some of which include signed kernels and modules, executable signing, and remote delegation of capabilities.

The proposed trust infrastructure manages trust delegation through public-key cryptographic signatures. It proposes a kernel-based interface for managing public key trust and verifying signatures at runtime, as well as a convention for defining the trust configuration when building a system from source. It includes a design for continuing a secure chain of custody from the boot loader through to the kernel and in to runtime, and includes several mechanisms for defining the root-of-trust for the boot loader and kernel. It also includes proposed standards for signing executables, as well as a tool for batch-signing and signing with ephemeral keys. Additionally, the proposed infrastructure is designed to integrate with and work alongside the NetBSD VeriExec infrastructure, and both systems benefit from doing so. Finally, the proposed infrastructure incorporates considerations for utilization of post-quantum cryptography in its design.

This talk is intended to be a review of the proposed design and to elicit serious consideration and feedback. Input and suggestions are welcome, and will be considered as possible modifications to the design.