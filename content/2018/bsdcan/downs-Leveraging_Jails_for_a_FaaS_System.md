---
layout: video
title: "Leveraging Jails for a FaaS System"
date: 2019-06-08
author: Brian Downs
email: brian.downs@gmail.com
youtube: XpdO3RaqXY4
---
Function as a service (FaaS) is the latest frontier of cloud computing freeing developers from writing more code than necessary and abstracting away discrete behavior. Jails provide a great abstraction between the host system and another separate execution environment. With FaaS concepts and jails, in conjunction with ZFS, these components can be leveraged to provide powerful, on-demand, dynamic binary executions with the safety and performance that jails offer.

We will go through system setup including package installation, jail creation, etc & show attendees how we can use jails for these purposes. We will use a proof of concept implementation that will be available on GitHub. I'd like to speak about this with the most broast strokes as possible so not to limit it to the view from that implementation, since the possibilities are endless. Another reason is to highlight that you don't necessarily need Docker to containerize your static or dynamic workflows.

We'll begin by going over what jails are and how they're traditionally used as well as what ZFS is. We'll talk about how the use of snapshots and clones are critical in achieving a clean environment for each function execution. Then we will venture into how jails can be used in a more on-demand way and look at how this is done using code. I'll provide this in a couple languages for as much context as possible but will reference the POC implementation for the full view. I'll get into the details of networking with jails and how to provide network access to those jails executing functions that need those resources. This will entail going over security concerns of enabling raw sockets or the necessity of building IP management into the system of which I have a very simple example.

Once the components themselves are understood and put together, I'll show how this all works, with a number of demonstrations highlighting the benefits of a this approach. As part of the demonstration, I'll show how a simple HTTP REST API can be used to trigger function execution and also provide insight into the system as well as administrative abilities.

The format of the talk would be a lecture and slides with live demonstrations but I'm happy to hear any and all suggestions.

I've been a FreeBSD user for around 10 years, using Jails a for a good portion of that time and using Go for the past 4. The combination of the two present a the portion of my free and personal time.

Git:  https://github.com/briandowns/sky-island