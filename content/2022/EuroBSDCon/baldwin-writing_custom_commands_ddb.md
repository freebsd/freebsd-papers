---
layout: slides
title: "Writing Custom Command in FreeBSD's DDB Kernel Debugger"
date: 2022-09-18
author: John Baldwin
youtube: sZMcVZjFW4g
---
FreeBSD's kernel includes an in-kernel debugger (DDB) inherited from 4BSD.
DDB's command interface provides limited capabilities for examining data, but
new commands can be added relatively easily to add pretty-printing of data
structures.  This talk goes over the basic APIs available to DDB command
handlers and how to register handlers as new commands.  It will also cover more
advanced topics such as manually parsing DDB commands to support richer command
arguments.
