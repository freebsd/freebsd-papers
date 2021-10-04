---
layout: slides
title: "logstor: A Log-structured user level GEOM layer"
date: 2021-09-19
author: Wuyang Chung
email: wy-chung@outlook.com
youtube: PoJXDeX9K-E
---

Most file systems today are write-in-place file system. This kind of file system
will generate random writes to the underlying storage device and random writes
are bad for both hard disk and flash disk. On the other hand, log-structured
file system is a copy-on-write file system. The new written data are appended to
the end of the log so it writes data sequentially. Logstor is a user level GEOM
layer that can be inserted between the file system and the storage device. It
uses the same principle of log-structured file system, that is the data are
always appended to the end of the log, so it can also transform random writes
from file system above to sequential writes to the underlying storage device.
Logstor can make any file system a log-structured file system when that file
system is created on it. Also if the logstor commands snapshot and commit are
implemented, it can make the file system run faster by not having to sync file
system’s metadata frequently.

Please check https://github.com/wy-chung/logstor for more detailed information.

**Wuyang Chung**

Wuyang Chung has been working in the IT industry for almost 20 years, currently,
working as a freelancer. Previously, Chung worked at Industrial Technology
Research Institute as a Windows CE system integrator. After that he worked in
ALi as a firmware engineer. His last work was in Hewlett-Packard Taiwan branch
as a system software engineer and worked on writing test programs and helping to
analyze product issues detected by these test programs.
