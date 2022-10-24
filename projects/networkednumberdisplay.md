---
title: Networked Number Display
description: 
published: true
date: 2022-10-19T12:40:31.583Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:53:27.898Z
---

# Networked Number Display

Because We can.

# Origins

Christopher Percival dropped off a 9 digit, 7 segment LED display at the space a while ago.

Brendan Ragan wanted a "kill counter" to use at various conventions for a game they are demonstration so we will be making a network-controllable number counter!

# Display info

The only parts of the orignal display that will be re-used are:

-   The 7 segment displays
-   The cathode driver transistors
-   The case

Everything else will be yanked and replaced with a driver/power board with a serial input consisting of:

-   an Arduino Pro Mini

The driver board will be connected to a Raspberry Pi which will provide the actual network interface and control the AVR driver via a serial link.

# Build Pictures

<img src="/projects/networkednumberpic1.jpg" width="200" /> <img src="/projects/networkednumberpic2.jpg" width="200" /> <img src="/projects/networkednumberpic3.jpg" width="200" />
