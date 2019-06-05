---
layout: video
title: "Replacing Traditional Backup Systems with ZFS: Using ZFS Snapshots and Replication to Simplify Backups"
date: 2018-06-09
author: Calvin Hendryx-Parker 
youtube: b9Hw2YjQv64
---
Consistent backups are vital to any operation. Making sure this process is simple is key to making sure it is done at all. Tools like Amanda and Bacula are sophisticated and complex tools that do the task, but they require care and feeding to ensure they work consistently. Leveraging the built-in features of ZFS such as replication and snapshots can greatly simplify the backup process.

Using portable management tools such as zfSnap and zxfer to manage backups across your infrastructure ensures that backups are done and can be even more granular than the typical daily/weekly backup schemes. We will look at using these tools from desktops to the server environment and how to have your backups easily distributed to multiple locations using FreeNAS’s scheduled tasks and replication.

We will explore how to easily keep rolling snapshots and replicate them to backup servers. Easily give the ability to rollback on a file servers to a snapshot taken within minutes instantly, but also allow long term snapshots to be kept and replicated efficiently to backup volumes. We will also cover deployment techniques to ensure that systems have the correct packages installed and configured via configuration management.

zfSnap: https://www.zfsnap.org/
zxfer: https://github.com/allanjude/zxfer
Salt Configuration Management: https://www.saltstack.com/resources/community/
