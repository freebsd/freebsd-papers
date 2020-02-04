---
layout: video
title: "Improving security of FreeBSD with TPM 2.0 and Intel SGX" 
date: 2019-09-21
author: Kornel Dulęba
email: kornel@duleba.com.pl
youtube: CEEBLke82_E
---
The talk describes the concepts behind TPM, together with a short introduction to Intel SGX.

TPM 2.0 devices are now supported in FreeBSD. They are most often referred to in the context of measured boot, i.e. secure measurements and attestation of all images in the boot chain. The TPM 2.0 specification defines versatile HSM devices which can also strengthen security of various other parts of your system. I will describe the basic features of TPM and mention some caveats and shortcomings which may have contributed to its limited adoption. The presentation will include practical TPM use cases such as hardening Strongswan IPSec tunnels by signing with the TPM and locking in secrets to a particular boot hash chain.

The second part will describe Intel SGX – a hardware based Trusted Execution Enviroment. (TEE) It will be started with describing basic concepts behind TEEs and SGX in particular. Next security advantages of using SGX will be discussed, as well as some of the vulnerabilities inherited from the past. The presentation will be concluded with a short report about SGX support in FreeBSD.

**Kornel Dulęba**

Jagiellonian University student and software developer working for Semihalf. He specializes in operating systems and security. He made multiple contributions to FreeBSD project including writing TPM 2.0 driver from scratch.
