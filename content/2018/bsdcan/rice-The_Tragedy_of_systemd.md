---
layout: slides
title: "The Tragedy of systemd"
date: 2018-06-08
author: Benno Rice
email: benno@FreeBSD.org
youtube: 6AeWu1fZ7bY
paper: rice-The_Tragedy_of_systemd.pdf
---
systemd is, to put it mildly, controversial. Depending on who you ask it's either a complete violation of the UNIX philosophy, a bloated pile of bugs, a complete violation of the elegant simplicity it replaced or, it most cases, some or all of the above.

So why have so many Linux distributions taken to it? Is it as bad as people say? Are the BSD projects right to be avoiding it?

Let's look into the history of UNIX userland bootstrapping and the factors that lead to the creation of systemd, why it's turned out the way it has, and what there is to be learned from it.

Clickbaity title ahoy!

This talk is about why something like systemd came to be. It looks into the history of system bootstrap over various UNIXes (and others), then looks at macOS and launchd before drawing direct parallels from launchd (and its cohorts) to systemd. From there it looks at why the ideas behind systemd are largely beneficial and the things it does better than what came before it, including the notion that "service management" is an underdeveloped concept on a lot of UNIXy systems and that it extends well beyond bootstrap to the entire system lifecycle.

Then, in order to bring it all back down to earth, the talk discusses what systemd gets wrong before moving on to the actual tragedy of the piece: That the people behind systemd seem largely ill-equipped to manage the social aspect of the level of change they're pushing and that this could sour large groups of people on the entire idea of something like systemd. It ends with a discussion of how FreeBSD (or other BSDs) could implement the ideas behind systemd in better ways.