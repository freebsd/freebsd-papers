---
layout: paper
title: "Improving security of the FreeBSD boot process"
date: 2019-03-24
author: Marcin Wojtas
email: mw@freebsd.org
paper: wojtas-Improving_security_of_the_FreeBSD_boot_process.pdf
---
## Improving security of the FreeBSD boot process

The talk describes recent security additions in the FreeBSD boot process. It will describe describe UEFI Secure Boot support in the FreeBSD loader and kernel. The loader is now able to parse UEFI databases of keys and certificates which are used to verify a signed FreeBSD kernel binary, using BearSSL as the cryptographic backend. FreeBSD veriexec capability is employed to verify various userland binaries and conguration files - it was extended with the ability to use UEFI trust anchors as a base for veriexec manifest verification Additionally, TPM 2.0 devices are now supported in FreeBSD. They are most often referred to in the context of a measured boot, i.e. secure measurements and attestation of all images in the boot chain. The basic features of TPM will be described, as well as some caveats and shortcomings which may have contributed to its limited adoption. The presentation will include practical TPM use case, such as hardening Strongswan IPSec tunnels by performing IKE-related cryptographic operations within the TPM, using private keys which never leave the device.
