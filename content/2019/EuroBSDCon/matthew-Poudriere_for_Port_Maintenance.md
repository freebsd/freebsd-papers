---
layout: slides
title: "Poudriere for Port Maintenance"
date: 2019-09-22
author: Matthew Seaman
email: matthew@freebsd.org
---
This class will be complementary to Nicholas Zeising’s course on FreeBSD ports, which I believe he is also submitting. Ideally it should be scheduled so that a student could attend his class first, and then this one. However, having attended Nick’s course is only a recommendation, not a requirement.

This will be a hand-on practical class. Each student will be provided with access to a pretty-much virgin installation of FreeBSD 12 on amd64, and will build a poudriere server with multiple jail instances (combinations of FreeBSD i386 and FreeBSD amd64 architectures, and version 11.2 and 12.0 jails), nginx as a web front-end and a ports tree based on a working checkout from one of the project’s VCSes (git in this instance, although usage of SVN will be described.)

All of the above should be made fairly quick and tractable by applying the power of Ansible to automate the work. Students will be able to take away the playbooks for later use on their own systems.

We will then illustrate how to use this setup to test-build ports with modifications, what diagnostic information you can obtain from poudriere logs, how to debug build problems and what to do when what poudriere logs is not enough to solve them.

We will conclude by talking about how this setup fits into a full ports development and testing workflow, how it facilitates contributing changes back to the FreeBSD project and how it can be adapted for use as a private pkg(8) repository setup.
