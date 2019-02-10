---
layout: paper
title: Rethinking /dev and devices in the UNIX kernel
date: 2002-02-13
author: Poul-Henning Kamp
email: phk@FreeBSD.org
---
An outstanding novelty in UNIX at its introduction was the notion
of ‘‘a file is a file is a file and even a device is a file.’’ Going
from ‘‘hardware only changes when the DEC Field engineer is here’’
to ‘‘my toaster has USB’’ has put serious strain on the rather crude
implementation of the ‘‘devices as files’’ concept, an implementation
which has survived practically unchanged for 30 years in most UNIX
variants. Starting from a high-level view of devices and the semantics
that have grown around them over the years, this paper takes the
audience on a grand tour of the redesigned FreeBSD device-I/O system,
to convey an overview of how it all fits together, and to explain
why things ended up as they did, how to use the new features and
in particular how not to.
