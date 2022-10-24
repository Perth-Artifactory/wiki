---
title: EPROM Programming PC
description: 
published: true
date: 2022-10-19T12:46:08.417Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:55:26.439Z
---

# EPROM Programming PC

**Specifications**

-   EPROM reader/programmer: Sunshine EW-901BN
-   PC: 500MHz Pentium-III Compaq Deskpro DPENS with 128MB of RAM running Windows 98SE
-   Supported devices: 27(C)16 2kB — 27(C)512 64kB ROMs and 12.5V, 21V and 25V EPROMs
-   Supported modes: normal, intelligent and quick
-   Location: in the electronics area, near the server rack (it's the small, beige PC connected to the 20" NEC monitor)

***Very* Abridged Users Guide**

To read or write your ROM/PROM/EPROM chips, boot the PC and start the program by double-clicking on the EPROM Programmer icon on the desktop; you should see the following screen:

![](/tools/eprommer-start.png)

The first thing to do is select the type of EPROM; to do this, press the 'M' key. Unfortunately this programmer's software does *not* have an integrated parts database so you might need to track down the chip's datasheet --- in a pinch, though, 'general EPROM' should be fine if all you want to do is read its contents.

![](/tools/eprommer-manufacturer.png)

Next, select the EPROM size and programming voltage by pressing the 'T' key. The size, or 'type', should be pretty easy to pick. If you want to program the chip, then its datasheet will list the correct programming voltage; if you just want to read the EPROM then any voltage will do.

![](/tools/eprommer-type-select.png)

To image an already programmed ROM, press 'R' to read the chip's contents then '3' to save the buffer to disk. (The PC is on the network and it supports floppy disks and USB drives so getting files off or onto the machine should be pretty straightforward.)

![](/tools/eprommer-read.png)

To program a blank EPROM, press '2' to load the image from disk, 'B' to confirm that the chip is blank, 'P' to program it and 'V' to verify that the image was, in fact, successfully programmed. Oh, and if for some reason you weren't able to track down the correct datasheet, you can check ![this](/tools/eprom_programming_voltages.pdf) out; failing that, you can start with a programming voltage of 12.5V and increase it if if the chip fails to verify correctly.

The final option worth mentioning is the programming algorithm; in most situations, the 'Intelligent' mode should be fine, but to program some of the older chips you might need to select the 'Normal' mode.

![](/tools/eprommer-programming-algorithm.png)

**Resources and Further Information**

In the unlikely event that something goes awry, a copy of the programmer's software is available ![here](/tools/eprom-programmer-software.zip); more information about the programmer is available [here](http://www.danbbs.dk/~rmadrm/eprom9.htm). If that doesn't fix it, or if you're having trouble using this setup, feel free to contact Peter Dreisiger.

------------------------------------------------------------------------

This machine belongs to Peter Dreisiger is on loan to the Artifactory; please do not remove it from the space without first checking with him.
