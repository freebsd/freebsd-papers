---
layout: slides
title: "Writing FreeBSD IR driver for ARM boards"
date: 2017-03-12
author: Ganbold Tsagaankhuu
email: ganbold@freebsd.org
youtube: YUJdf-kioHg
---
There are various input devices including keyboard, mouse and touchscreens exist these days.
They need to have corresponding driver in operating system in order to work correctly.
Input drivers in FreeBSD still have a lot of room for improvement, especially for new types
of devices such as touchscreens and infrareds. This paper describes the possible way of 
writing input driver in case of Consumer IR (CIR) controller using new Evdev interface
recently committed by Oleksandr Tymoshenko. The paper also shows how to test CIR driver
and demonstrates the use of it on small ARM boards.
