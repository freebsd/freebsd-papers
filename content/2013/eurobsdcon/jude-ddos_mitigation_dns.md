---
layout: slides
title: "Mitigating and Isolating DDoS at Layer7"
date: 2013-09-29
author: Allan Jude
email: allanjude@freebsd.org
---
## Mitigating and Isolating DDoS at Layer7 using Global Server Load Balancing with gdnsd on FreeBSD by Allan Jude

An overview of our production implementation of the gdnsd DNS server on FreeBSD 9.x as a Global Server Load Balancer. We discuss how the GSLB can be used to mitigate and isolate distributed denial of service attacks without requiring extensive network infrastructure, cooperation from your transit providers, or BGP/Anycast. Coverage of the types of DDoS attack as well as the prevention and cleanup/prosecution steps. The talk will cover a number of different defensive techniques and then detail our solution using our GSLB.
