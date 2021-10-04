---
layout: slides
title: "A Carrier-Grade L2BSA Gateway with Netgraph"
date: 2021-09-19
author: Lutz Donnerhacke
email: donner@freebsd.org
youtube: UI5CD2_RXJ0
---

In Germany, broadband access is still based on copper to the house due to
historical, political reasons. In order to increase transfer rates vectoring
became ubiquitous. That’s why all wires between houses and a curb need to be
operated by a single company. Unfortunately, Germany does not distinguish
between layer2 operators and layer3 operators. So either all households have to
buy Internet from a monopolist or a layer2 transmission to a third party ISP
must be regulated. The regulated access to the layer2 bitstream of a customer is
defined by the regulation authority and implemented as a so- called A10NSP
gateway. In principle at this point all layer2 traffic is encapsulated by an
additional VLAN tag for each customer line. The VLAN tag itself is defined to be
fixed as long as the DSL is in sync, but will change randomly on resync.
Existing A10NSP solutions are expensive, closed appliances which provide only a
single type of access: PPPoE. We offer triple play via DHCP on multiple VLANs to
our customers, and we did not want to pay others for a (limited) solution. So
the idea arose to implement this A10NSP gateway ourselves using FreeBSD and
netgraph. At this time several thousand customers are connected using this cheap
and scalable solution.  Let’s have a look into the implementation.

**Lutz Donnerhacke**

Lutz Donnerhacke studied physics and mathematics. During this time he was part
of the Internet build-up (Individual Network) in Germany and administrator of
the USENET de-hierarchy. Interest focused on cryptography (OpenPGP, X.509,
DNSSEC), programming (Ada, Haskell, Piet, C, Perl, PHP), and Internet governance
(Fitug, ICANN). He is working for a regional ISP for more than 20 years and
currently active in building central infrastructure for a larger ISP.
