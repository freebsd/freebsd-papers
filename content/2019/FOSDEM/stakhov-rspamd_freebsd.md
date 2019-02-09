---
layout: slides
title: "Rspamd integration into FreeBSD.org mail infrastructure"
date: 2019-02-02
author: Vsevolod Stakhov
email: vsevolod@rspamd.com
video: https://video.fosdem.org/2019/K.3.401/rspamd_integration_freebsd.mp4
---
After years using SpamAssassin on FreeBSD.org, we have moved towards Rspamd last year to improve spam filtering and integrate it as milter to postfix. With this step we could impressively drop spam rate and increased performance comparing to SpamAssassin.

In this presentation, we plan to describe the current architecture of the email system and how Rspamd fits into it. Then we will describe the main challenges for AS system when dealing with lots of technical discussions and mailing lists. We will also explain the unique features of Rspamd and cover the outstanding issues (e.g. with DKIM).
