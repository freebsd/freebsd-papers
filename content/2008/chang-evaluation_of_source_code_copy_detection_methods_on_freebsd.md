---
layout: paper
title: "Evaluation of Source Code Copy Detection Methods on FreeBSD"
date: 2008-05-10
author: Hung-Fu Chang
email: hungfuch@usc.edu
paper: chang-evaluation_of_source_code_copy_detection_methods_on_freebs.pdf
---
Studies have shown that substancial code reuse is common in open source and in commercial projects. However, the precise extent of reuse and its impact on productivity and quality are not well investigated in the opensource context.
Previously, we have introduced a simple-to-use method that needs only a set of file pathnames to identify directories that share filenames and partially validated its performance on a set of closed-source projects.
To evaluate this method and to improve reuse detection at the file level, we apply it and four additional file copy detection methods that utilize the underlying content of multiple versions of the source code on the FreeBSD project.
The evaluation quantified unique advantages of each method and showed that the filename method detected roughly half of all reuse cases. We are still faced with a challange to scale the contents based methods to large repositories containing all versions of open source files.
