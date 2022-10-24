---
title: Open Door Control
description: 
published: true
date: 2022-10-19T12:40:44.631Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:53:47.556Z
---

# Open Door Control

An access control system with RFID reader, an electronic lock, battery backup, log files, two line LCD panel, and blinken-lights.

## Hardware

### v1.0

-   Functional Prototype
-   Currently installed, mission-critical hardware

|                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------|
| \< 100% 30% 50% \>                                                                                                        |
| Part                                                                                                                      |
| [Freetronics EtherMega](http://www.freetronics.com/products/ethermega-arduino-mega-2560-compatible-with-onboard-ethernet) |
| microSD card                                                                                                              |
| [ID-12 125 kHz RFID Reader](http://www.sparkfun.com/products/8419)                                                        |
| [DS1307 RTC on Breakout](https://www.adafruit.com/products/264)                                                           |
| FIXME                                                                                                                     |

#### Gotchas

-   Hordor
-   The SDCard reader software appears to have a limit on the number of files it supports (although it may be in our github code) If in doubt, delete all LOGFFFF.TXT files before rebooting.

#### Software

The source will be available at <https://github.com/Perth-Artifactory/OpenDoorControl>

### v2.0

-   Currently in design phase based on v1.0

|                    |
|--------------------|
| \< 100% 20% 20% \> |
| Component          |
| Raspberry Pi       |
| LM22678TJ-5.0      |
| TLC5951            |
| ID-12              |

## TODO/Desired Features

|                                                         |
|---------------------------------------------------------|
| \< 100% 35% \>                                          |
| Feature                                                 |
| 60 second post lockup grace period                      |
| Access list updated over Ethernet (from LDAP via HTTP?) |
| State change notification over Ethernet/HTTP            |

Version 2 progress is being tracked at <https://github.com/Perth-Artifactory/doorbot>

## Photos

FIXME
