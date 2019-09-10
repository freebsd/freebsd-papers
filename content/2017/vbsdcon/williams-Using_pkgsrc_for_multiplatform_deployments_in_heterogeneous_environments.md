---
layout: slides
title: "Using pkgsrc for multi-platform deployments in heterogeneous environments, Made to Measure: Network Performance Analysis in FreeBSD"
date: 2017-09-09
author: G. Clifford Williams
email: gcw@8ions.com
youtube: oqbUw8pxOJk
---
This talk covers the benefits of decoupling your application code from the packaging system that ships with your operating system. Unless the packaging system for your OS happens to be pkgsrc.

Need two incompatible versions of the same library installed on the same host? Want a different version of crypto libraries, compilers, or language runtimes than what comes out of the box with your default package manager? Docker style containers are currently all the rage but they come at a cost and with several layers of indirection. Here we'll talk about a much simpler approach to hosting multiple versions of the same applications, tools, libraries, etc in a conflict-free manner with the help of pkgsrc.

Specifically we'll look at the reduced complexity in using tools like Salt, Chef, Ansible, and Puppet for orchestration and configuration management as well as ways to avoid the administrative overhead of using Jails, Zones, and LXC.