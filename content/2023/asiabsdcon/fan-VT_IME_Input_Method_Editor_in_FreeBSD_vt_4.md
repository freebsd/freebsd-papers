---
layout: paper
title: "VT-IME: Input Method Editor in FreeBSD vt(4)"
date: 2023-04-02
author: Fan Chung
email: fan@freebsd.org
paper: fan-VT_IME_Input_Method_Editor_in_FreeBSD_vt_4.pdf
---
In this paper, we proposed vt-ime framework, which provides an environment for users to type CJK characters in the virtual terminal vt(4). The vt-ime framework is composed of two parts: the vt-ime backend and the frontend. The backend listens for key events sent from the frontend and uses an input method library, such as librime, to translate these key events into valid CJK characters. The processed characters are then sent them back to frontend for rendering. The frontend, which runs inside vt(4), is responsible for rendering the virtual terminal and displaying the CJK characters on screen.
