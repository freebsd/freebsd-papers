---
layout: slides
title: IT automation with Puppet
date: 2018-06-09
author: Romain Tartière
email: romain@
youtube: Cb4VmhuyIMo
video: optional-link
---

Puppet is a Free/Libre configuration management tool. Rarely used standalone,
Puppet is generally the core of a more complex setup used to manage an
organization's computers. As a consequence, each organization has it's own set
of tools and workflows; and when discovering Puppet for the first time, you
might get scared by the number of different resources explaining how to do
similar things in slightly (and sometimes very) different ways. In this talk,
you will learn the fundamentals of Puppet, you will be introduced to some of
the tools often found in a Puppet setup, and understand how these tools share
responsibility to configure all the nodes you are in charge of.

The following topics will be covered:

* Puppet itself
* Puppet Modules and the Puppet Forge
* Facts
* Hiera
* r10k
* control-repo
* The Roles and Profiles pattern
* PuppetDB
* External Node Classification
* Marionette Collective
* Choria

And that's a lot! So, in order to make this easier to digest, all these tools
will not be introduced one after the other independently; but rather introduced
when they become useful in the deployment of Puppet in a fictive company that
was not using configuration management before.

This will help you to determine which tools might be useful when building your
IT automation infrastructure, and schedule the next steps for bringing-in
Puppet to your workplace (or home).

Last but not least, Puppet is cross-platform, but since we are in a BSD-centric
conference, a particular emphasis will be put on \*BSD operating systems.

