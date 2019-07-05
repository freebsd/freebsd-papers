---
layout: paper
title: "Improving security of the FreeBSD boot process: TPM and Secure Boot in FreeBSD"
date: 2019-05-17
author: Michal Stanek
email: mst@semihalf.com
paper: stanek-Improving_Security_of_the_FreeBSD_Boot_Process-paper.pdf
youtube: kgq3y4fCWWc
---
The talk describes recent security additions in the FreeBSD boot process.

TPM 2.0 devices are now supported in FreeBSD. They are most often referred to in the context of measured boot, i.e. secure measurements and attestation of all images in the boot chain. The TPM 2.0 specification defines versatile HSM devices which can also strengthen security of various other parts of your system. We will describe the basic features of TPM and mention some caveats and shortcomings which may have contributed to its limited adoption.

The presentation will include practical TPM use cases such as hardening Strongswan IPSec tunnels by signing with the TPM and locking in secrets to a particular boot hash chain.

The second part of the talk will describe UEFI Secure Boot support in the FreeBSD loader and kernel. The loader is now able to parse UEFI databases of keys and certificates which are used to verify a signed FreeBSD kernel binary, using BearSSL as the cryptographic backend.

The talk describes recent security additions in the FreeBSD boot process.

TPM 2.0 devices are now supported in FreeBSD. They are most often referred to in the context of measured boot, i.e. secure measurements and attestation of all images in the boot chain. The TPM 2.0 specification defines versatile HSM devices which can also strengthen security of various other parts of your system. We will describe the basic features of TPM and mention some caveats and shortcomings which may have contributed to its limited adoption.

The presentation will include practical TPM use cases such as hardening Strongswan IPSec tunnels by performing IKE-related cryptographic operations within the TPM, using private keys which never leave the device. Another example will be sealing secrets in TPM NVRAM with specific boot measurements (hashes) stored in PCR registers so that the secrets are locked in to a specific boot chain.

The second part of the talk will describe UEFI Secure Boot support in the FreeBSD loader and kernel. The loader is now able to parse UEFI databases of keys and certificates which are used to verify a signed FreeBSD kernel binary, using BearSSL as the cryptographic backend.