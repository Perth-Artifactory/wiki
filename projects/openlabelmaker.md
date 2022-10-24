---
title: Open Label Printer
description: 
published: true
date: 2022-10-19T12:40:51.340Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:53:56.732Z
---

# Open Label Printer

(currently out of date: Vincent Dalstra has an up to date specification)

## Goals

-   Make it easier for people to label their stuff.
-   Lets people make nice labels for other purposes.
-   Adhesive business cards, anyone?
-   Labelling lots of things quickly (e.g. instructions for catapults; cuts down to a nice size).

## Initial functionality

##### Things that will work ‘out of the box’.

-   Printing of simple text labels via Web tool. (smartphone compatible).
-   Printing images via a linux command-line tool (aim to make this easier)

## Desired functionality

i.e. things that require software modification in order to get working.

-   Printing images via the web tool.
-   Automatically print Name/Date Labels when an RFID key is scanned.
-   Generate and print QR codes via the web tool
    -   Provide a guide to make generators for similar things e.g. chip pinouts.
-   Printing multiple copies of a label via the web tool.

## Costly Materials (\$142)

-   Label printer (QL-700) \$99
-   Raspberry pi, with wireless (easier to position) + usb mini to usb large adaptor \$21 + \$5 <https://core-electronics.com.au/raspberry-pi-zero-w-wireless.html>
-   Micro-SD card (for the pi) \$8.50
-   RFID reader + Interpreter (arduino nano) \$5.50 + \$3.00

## Possible assistance needed with:

-   Reading names from RFID (is it stored on the chip, or do I need to query a server?)
-   Also need to know the correct RFID reader to use, and how to connect it to a raspberry pi; a problem that has already been solved with doorbot.
-   If it used NFC (as I suspect it it does) then I should be fine
-   Setting up a raspberry pi (I’ve never done it before – should be easy, but someone else’s expertise might save time/headaches).
-   Modifying the web tool (the webserver printing tool is good, but could benefit from some modifications; luckilyit is written in python, which I’m not familiar with)

## Printer specs

#### Brother QL- 700

-   \$100 + \$1.62per metre (60mm wide tape, official)
    -   Aftermarket: 20c per metre (Amazon)
-   13 cm/s print speed - for 30 x 60 mm ‘standard address labels’ (5c per label, official).
-   Can print sideways (min. print 12.7mm). Retracts from cutter to avoid wasting space.
-   Autocutter – multiple labels at once.
-   Local Return (officeworks), just in case it’s not up to snuff.
-   There is a guide for combining a raspberry pi with this printer. It can also host a browser-based label design tool (works on smartphones too). <https://www.rs-online.com/designspark/building-a-pi-powered-wireless-label-printer>
-   Actually bypasses the official drivers entirely.
-   Videos in action: (some variation in speed: worth investigating). Resolution is very good.
    -   <https://youtu.be/lNq2BLUgmrA?t=253> (printing slowly)
    -   <https://youtu.be/h62ECk2arUw> (seems more like the claimed speed; very fast).

## Alternative printers that were considered:

### Brother PT-P700

-   \$80 + \$0.60 per meter (24mm wide tape, same price for thinner – down to 8mm)
    -   PS: This is the aftermarket price
-   Print speed not stated
-   Uses thin tape up to 24mm wide
-   No official linux drivers, but seems to be CUPS compatible (See comments at <http://www.openprinting.org/printer/Brother/Brother-PT-P700>)
-   Local Return

### Dymo 450

-   \$94
-   No Autocutter; (rip-strip instead). Not as neat, and inconvenient for many labels.
-   Rumoured to have more after-market label options (extra colours etc.)
-   Has also been used in similar projects.
