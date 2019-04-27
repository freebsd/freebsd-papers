---
layout: slides
title: "Forget reusability, aim for perfection: New lessons from mandoc development"
date: 2018-06-08
author: Ingo Schwarze
email: schwarze@openbsd.org
youtube: N26pBxJPMxs
paper: schwarze-new_lessons_from_mandoc_development.pdf
---
Many new features and applications have been developed with the mandoc(1) manual page toolbox during the last three years, including a new database backend, a markdown output mode, much improved WWW output and roff(7) and ports handling, the application to LibreSSL documentation, and more. I'll provide an overview and explain what we learnt from these projects.

At BSDCan 2015, i explained how mandoc(1) managed to become the standard BSD manual toolbox both for the command line and for the web. So you might think it is now finished and nothing more was done during the last three years. But that's far from the truth!

We can still learn a lot both from developing it further and from applying it to large-scale real-world tasks. I will present lessons from five quite different larger projects completed in and with mandoc in 2016 and 2017, and from several smaller ones, and i will show that we are not quite done yet and worthwhile tasks remain.

The major topics are:

1. Deletion of SQLite from the OpenBSD base system (July 16): why that was done, what the immediate benefits for mandoc are, and what that teaches us. Among other points, this is where the deliberately provocative title comes from: maybe you should not completely forget about reusability, but it is definitely over-valued nowadays, both when designing new code and when choosing third-party components to employ.

2. mdoc(7) conversion and polishing of LibreSSL manuals (Nov 16 to Jan 17): Tools used, additional work that was done by hand, current state of affairs, ongoing maintenance, what is still missing, and lessons learnt from that work - not only about mandoc, but also some about LibreSSL and about library design in general.

3. Improvements of WWW online manuals (e.g. man.openbsd.org): Lots (more than ten) different important improvements were implemented here in 2016/17 alone, not counting minor ones. While each single step may seem of easily manageable size and difficulty, i think the end result is something to be proud of, and that is being noticed even beyond the BSD world: Both Debian and Arch Linux now also use the mandoc formatter for their official online manuals.

4. The new markdown output (Mar 17) does not only demonstrate how simple it has become to implement a new mandoc output mode, but also how a markup language should not be designed and which kinds of tools you should not use for your documentation.

5. Parser unification and coping with ports (Apr to June 17): Reorganizing the parsers such that syntax tree nodes can now be generated on the roff(7) level allowed implementing lots of new roff(7) requests and escape sequences (ab)used by some third party man(7) pages in ports. Together with rather tricky improvements in the tbl(7) formatter, this allowed reducing the number of OpenBSD ports that still USE_GROFF from over 200 to just 25.

Even more than such major new features, successful maintenance really means taking care of lots and lots of small things including keeping up with newly developed security features, moving ahead with regression testing, coordinating with other implementations of the languages in question (in this case, mainly groff), further improving search and diagnostic functionalities, and more. There won't be time to discuss all that in detail, but i'll briefly mention about a dozen specific examples, and why they matter - for active maintenance of free software in general.

http://mandoc.bsd.lv/