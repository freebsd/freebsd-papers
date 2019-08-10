---
layout: video
title: "Transport Evolution on top of the BSD's"
date: 2017-02-04
author: Tom Jones
email: tj@freebsd.org
video: https://video.fosdem.org/2017/K.3.201/transport_evolution_bsd.mp4
---
##A New, Evolutive API and Transport-Layer Architecture for the Internet

Internet Transport is changing, some changes have been incremental updates to mechanisms (e.g., RACK, BBR), others demand new protocol options (e.g., MPTCP) or entirely new protocols (e.g., QUIC, SCTP). However significant changes are still difficult to deploy - requiring modifications to application code and support by the stack. Even when updates happen, the network needs to support the new method to allow applications to use it. Long deployment times have motivated the need to change how protocols are handled in the stack. We review the state of the art in Internet Transport, and the status of deployment in th BSD's and then propose a new direction for the transport interface, developed in the EU NEAT Project, that can ease deployment of new transports across all platforms. We conclude by showing the advantages and its prospects for standards adoption.
