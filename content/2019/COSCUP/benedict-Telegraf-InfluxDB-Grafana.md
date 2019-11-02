---
layout: slides
title: "Monitor your Systems with Telegraf, InfluxDB, and Grafana-A FreeBSD-focused Howto"
date: 2019-08-18 14:00 ~ 14:40
author: Benedict Reuschling
email: bcr@FreeBSD.org
---
System administrators often need to know what their systems are doing at a glance. A comprehensive monitoring solution periodically collects data from machines and sends them to a central database. From there, visualization tools take the data and create comprehensive graphs to make sense of the data.

In this tutorial-style talk, I will walk through the setup of such a monitoring solution on FreeBSD. Telegraf will be used to collect the data and send it to InfluxDB. Grafana reads from the database and present the data as customizable dashboards. The setup is quick and easy enough to get started and provides the system administrator with valuable information about their systems (CPU, memory, I/O, network usage, etc). All the software is available as open source and all configuration steps will be provided to the audience.
