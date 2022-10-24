---
title: The Gadget
description: 
published: true
date: 2022-10-19T12:42:41.716Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:56:40.213Z
---

# The Gadget

## Project Brief

The goal is to create a scientific sampling & diagnostic machine, PDA-esque device and generally cool gizmo in a small, preferably wearable form factor.

## Parts

|                             |
|-----------------------------|
| \<90%\>                     |
| Main Components             |
| Core                        |
| Main Board                  |
| FPGA                        |
| Built in Sensors            |
| Temperature & Humidity      |
| Barometric Pressure         |
| Infrared Thermometer        |
| Magnetic Flux Sensor        |
| Accelerometer               |
| Gyro                        |
| GPS                         |
| Camera                      |
| Pulse Oximeter              |
| Electronic Diagnostics Pack |
| ADC                         |
| Fast digital I/O            |
| Low speed digital I/O       |
| Built in Output Devices     |
| 4.3" LCD                    |
| DACs                        |
| Line Laser                  |
| Point Laser                 |
| 3W RGB LED                  |

| Power Supply                         | Model \# | Notes                                  |     |     | Cost |     |
|:-------------------------------------|:---------|:---------------------------------------|-----|-----|------|-----|
| Li-Poly RC car battery               |          | With quick-release, firewalls etc.     |     |     | \$60 |     |
| Switched mode power supply module    |          | Recom 9-36V in, 5V out                 |     |     | \$20 |     |
| current limits / under-voltage trips |          | custom (bullet-proof) BJT latch + fuse |     |     |      |     |

## Progress

The Gumstix overo-fire and chestnut43 boots from an RC car battery with 5V SMPS and an over-current under-voltage lockout circuit (set to \<1A, \>9V on the 11.1V input rail, schematics coming soon!)

The Gumstix system consumes about 0.45A at 12V. Far too much for a portable device, but most of that is the LCD back-light.

Oddly, the Gumstix module refuses to connect to a USB device without a USB hub (powered or unpowered) so the gadget will have multiple USB sockets, some populated by internal devices.

An Arduino pro-mini will be used (for now) to control the sensors and output devices. The final version will probably use a low-power micro-controller for data logging, power management and anything an OS isn't required for (whatever I can be bothered hard-coding on a micro) The pro-mini currently collects data from a barometer, humidity sensor and a magnetometer and displays it on a character LCD.
