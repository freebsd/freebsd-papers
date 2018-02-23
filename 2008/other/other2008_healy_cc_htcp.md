---
layout: paper
title: An Independent H-TCP Implementation under FreeBSD 7.0 – Description and Observed Behaviour
author: Jeff Healy
email: jhealy@swin.edu.au
paper: /_assets/other2008_healy_cc_htcp.pdf
---
A key requirement for IETF recognition of new TCP algorithms is having an independent, interoperable implementation. This paper describes our BSD-licensed implementation of H-TCP within FreeBSD 7.0, publicly available as a dynamically loadable kernel module. Based on our implementation experience we provide a summary description of the H-TCP algorithm to assist other groups build further interoperable implementations. Using data from our live testbed we demonstrate that our version exhibits expected H-TCP behavior, and describe a number of implementation-specific issues that influence H-TCP’s dynamic behavior. Finally, we illustrate the actual collateral impact on path latency of using H-TCP instead of NewReno. In particular we illustrate how, compared to NewReno, H-TCP’s cwnd growth strategy can cause faster fluctuations in queue sizes at, yet lower median latency through, congestion points. We believe these insights will prove valuable predictors of H-TCP’s potential impact if deployed in consumer end-hosts in addition to specialist, high-performance network environments.
