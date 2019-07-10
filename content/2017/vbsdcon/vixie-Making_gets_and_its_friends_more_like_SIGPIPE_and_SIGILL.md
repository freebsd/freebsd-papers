---
layout: video
title: "Making gets() and its Friends more like SIGPIPE and SIGILL"
date: 2017-09-09
author: Paul Vixie
email: paul@redbarn.org
youtube: Vr_T5hFtyoM
---
In the decades since the Morris worm, BSD has substantially modernized, which has included tracking ANSI C and POSIX LibC. Portability was seen as necessary for relevance and success, and for the most part, it has been. There are some exceptions, and it's long past the time when we should have made some hard but sensible choices about what to include or emulate, and what to leave out, and what to poison outright.