---
layout: slides
title: "Master & Minions or the Dream of BSD Automation: Using Salt and Python to manage the a BSD Cloud"
date: 2019-05-17
author: Calvin Hendryx-Parker
email: calvin@sixfeetup.com
youtube: rBvN242etK8
---
In this day and age, using hand-crafted servers is quickly becoming a losing proposition. Debugging a Python application that runs on custom made servers gets extremely tricky, and since apps no longer run on a single server, releases become increasingly resource intensive. It is therefore vital to have a process to control multiple FreeBSD servers simultaneously in the cloud from a single command. This talk goes through real life and practical examples to roll out orchestration and configuration management projects using Salt on FreeBSD.

After going over the pains of manual deployments, we will introduce the open source tools Saltstack and Cloud Custodian to automate the management of FreeBSD servers in a public cloud. We will then walk attendees through a real case study to give a practical understanding of what rolling out orchestration and configuration management means. We will end with hard learned tips to guard against common pitfalls.

Saltstack is a event-driven orchestration and configuration management platform written in Python. It lets you run a command across thousands of servers at once through its remote execution function. Its master can listen to events such as user logins or CPU usage thresholds and automatically have minions take corrective actions.

Cloud Custodian is an event-driven compliance platform that was originally developed in Python by Capital One. It allows for an organization to ensure compliance in its cloud infrastructure via policies. Cloud Custodian can make sure the correct encryption keys and ciphers are used. It can ensure new applications are always built on the latest machine images. Cloud Custodian can dramatically reduce costs by automatically removing unused cloud resources.

With a mandate to migrate all of their applications to the AWS public cloud, the client had to find a way to move their highly custom website hosted on FreeBSD.

We used Salt to build the new cloud infrastructure using the APIs provided by AWS. It allowed Notre Dame to deploy new environments for testing or, in an emergency, spin up instances in another region that match identically the current production environment. We also used Salt to power the release process so that the web team can release to the multiple servers that make up the environment with one single command orchestrated from the Salt master. They do not have to have deep knowledge of the servers and command line to release changes to the site.

Upfront choices about the operating system or distribution are critical to making this process of deploying simpler. The natural choice for deploying onto AWS might be to use Amazon Linux, but it turns out it has an older, more limited package manager. If you are expecting to use newer features of certain software such as HAProxy, you will need to ensure your distribution supports it out of the box. Managing extra builds and compiling from source is a short term solution as it will add the overhead of maintaining the environment.