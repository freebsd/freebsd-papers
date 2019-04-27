---
layout: slides
title: "ZFS send and receive, performance issues and improvements: Encryption, pipes and context switches need to go!"
date: 2018-06-08
author: Rodney W. Grimes
email: rgrimes@FreeBSD.org
youtube: ngk84blmbek
paper: grimes-zfs_send_and_receive_performance_issues_and_improvements.pdf
---
Traditional Unix pipes are not known for their high performance. Designed for use for "piping" text between commands, they have been put to use in ways far in excess of their original design. One such use is for local and network "ZFS send" which is the mechanism that the OpenZFS file system uses to transfer file systems and snapshots of file systems between one another. This talk will present a new ZFS send and receive that relies on network sockets rather than pipes.

Three things are to be discussed:

1) The local use of zfs send | zfs receive.

Due to context switching and data copying between the kernel and user process for each buffer of data there are changes that can be made to the pipe code to improve performance.

2) The remote use of zfs send | ssh zfs receive, and zfs send | nc

The selection of encryption protocols can have a significant impact on performance when using ssh as a transport, in many cases you only need authentication, and in some cases you just need to transport the data over the network.

3) A new option to zfs send and receive, socket.

The in kernel implementation of zfs send and receive uses a file descriptor for the read and write of data, by adding socket setup code to the zfs(8) command many of the performance issues no longer exist. Data is transported using the networking code purely within the kernel, no context switches or copy out and in from the user context occur reducing the load on the CPU.