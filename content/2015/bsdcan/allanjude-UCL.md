---
layout: paper
title: Universal Configuration Files
date: 2015-07-01
author: Allan Jude
email: allanjude@freebsd.org
youtube: 8l6bhKIDecg
---
Most system administrators no longer edit configuration files by hand, they use automation and configuration management tools.
Most utilities and daemons in the base system use their own custom configuration file format.
To solve this, I propose teaching the various utilities and daemons in the FreeBSD base system to speak UCL -- the Universal Config Language, as implemented by libucl.

Space and tab delimited files make it harder to extract a specific value, and difficult to edit that value in place, whereas nested key-value pairs are easier to read, and are easily addressed using libUCLs dotted notation.
While these various different formats are usually accompanied by man pages, they do not lend themselves to automation or programmatic editing.
In addition, I propose adding two small tools to the base system to make the administration of such config files easier for humans and automated scripts.

As the deployment of servers and applications becomes more transient, the practices of system administrators have needed to adapt to be more agile.
UCL (Universal Config Language) is an effort to define a modern configuration syntax and implement a library to parse it, that can be reused by many different applications to simplify administration.
Inspired by the NGINX and bind syntax, with elements borrowed from JSON, UCL strives to strike a balance between human writability, machine readability, and compatibility with existing formats.
libUCL can read UCL, JSON, and YAML, parse them into objects that can be read or manipulated, then emit the resulting objects back out in any of the three formats.

Convert these config files to UCL:

* newsyslog
* crontab
* iscsi / ctld
* autofs
* freebsd-update
* portsnap
* jail.conf (need support for variables like ${host.hostname} in path, has keys with dots in them)
* devd.conf (syntax doesn't match well, will need work)
