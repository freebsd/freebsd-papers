---
layout: paper
title: "diskctl(8): A permissively-licensed S.M.A.R.T. and raw disk command utility framework"
date: 2016-03-12
author: Michael Dexter
email: dexter@freebsd.org
youtube: RHvATmJMe7E
---
The Self-Monitoring, Analysis and Reporting Technology or S.M.A.R.T., is an industry-standard interface implemented by manufacturers of hard disk and solid-state drive devices to present device “health” information to the controlling operating system. This information can include device identification and configuration information, service hours, temperature, failed block reallocation counts, Solid State Disk (SSD) endurance remaining, plus vendor-specific attributes. These attributes are commonly accessed from various operating systems using the “smartmontools” project and specifically the smartctl(8) command. While popular, the smartmontools project does not feature a license suited for inclusion in BSD Unix operating systems, does not support NVMe devices, and is limited in its output formatting abilities. The diskctl(8) project aims to provide a framework to address the licensing and output formatting limitations of smartmontools and provide a user-friendly framework for new device types and output formatting syntaxes. Also, diskctl(8) aims to provide an interface to common ATA management commands such as IDENTIFY, plus the acoustic and power management series of commands. Finally, the diskctl(8) project will explore the possibility of supporting VirtIO AHCI S.M.A.R.T. and underlying zpool(8) status pass-through for virtual machine disk devices, and other virtualized storage opportunities.
