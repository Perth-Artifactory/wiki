---
title: musicalcoildriver
description: 
published: true
date: 2022-10-19T12:40:25.883Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:53:18.419Z
---

Related Projects: [Arcophone](arcophone) \| [Jacob's ladder](jacobs_ladder)

# Musical Coil Driver

## Pre-Orders

We are now taking pre-orders for version 2.0 of the driver board, this revision features and all new oscillator based on the MCP6542 dual comparator chip that is capable of a whole bunch more interesting high-voltage projects.  
[Details Here](http://www.artifactory.org.au/kits/coildriver/)

## Project Summary

Bored with your old synth? Think most MIDI output devices are just *so* last millenium? What you need is the Artifactory's very own 30,000 volt musical ignition coil driver!  
==== Licensing ==== The Coil Driver Kit is licensed under the TAPR Noncommercial Hardware License.  
\*\* Design files will be published before we sell any. \*\* We are holding off putting the design files up online until after we are satisfied that the design is both safe and operating within acceptable parameters.

### Some History

[SKoT](/User/skot) decided that the hackerspace needed something that went ZAP, in aid of this he acquired a Silicon Chip magazine jacobs ladder kit and commanded that his minions [Brett](/User/bdowning) & [Daniel](/User/atrophy) immediately set to work. Less than an hour after its completion, it was decided that it was lacking something, and that something was the capacity to play Tchaikovsky's 1812 overture alongside our internet-controlled smoke ring cannon (set to play the part of the cannons in the crescendo!) which had been completed a week earlier. Some burns, minor nerve damage and lacerations later, a working solution was discovered by bypassing the kit's ubiquitous 555 timer and inserting an opto-coupler allowing the connection of a [Freetronics TwentyTen](http://www.littlebirdelectronics.com/products/Freetronics-TwentyTen.html). Shortly thereafter a hardcoded version of the Star Wars Imperial March could be heard throughout the Artifactory and by anyone trying to listen to an AM band radio. Could this be it? Our goal achieved, NO, the notes were sour, crackling feebly in the slightest draught, the age old catch cry was heard, MORE POWER! And so was born the project you see chronicled here, the quest for crisp notes and robust arcs, the Musical Coil Driver.

### Software

SKoT, being the preeminent master of all things MIDI that he is, has allowed our high voltage villainry to work seamlessly(ish) with a MIDI keyboard.

## Prototype Testing Log

| Version | Notes                                                           | Known Issues                                                            |
|---------|:----------------------------------------------------------------|:------------------------------------------------------------------------|
| 0.0     | Assembled Silicon Chip magazine kit                             | Not Musical, otherwise **very** rugged                                  |
| 0.0a    | Hacked into SC kit to use external oscillator w/ opto isolation | Musical range very limited, these coils should be driven harder!        |
| 0.1     | First Artifactory design based on FET                           | Prone to thermal failure from switching loss                            |
| 0.2     | Second Artifactory design with push/pull FET driver             | Thermal stress still unacceptable due to coil saturation                |
| 0.2a    | Revision to up resistance on R5 from 0.47Ω to 1Ω                | Transient loads on PSU unacceptable                                     |
| 0.2b    | Added power buffer capacitor 4700uF 16v                         | IGBT susceptible to ESD                                                 |
| 0.2c    | Included gate protection zener (as recommended in datasheet)    | No known issues, advanced to v1.0 for pilot production and beta testing |
| 1.0     | First production kit!                                           | Thermal Issues on 10w Resistor                                          |
| 1.1     | Fixed issues with v1.0, added indicator LED's                   | None found                                                              |
| 1.2     | Added onboard oscillator circuit, sending for prototyping.      |                                                                         |

### Notes

Extensive **destructive** testing has resulted in 3 failures of the IGBT, each with a confoundingly different failure mode. Thermal failure in v0.1 due to switching loss resulted in SCR like behaviour but not a *full* failure, rectified by improved driver design (v0.2).  
  
ESD damage in v0.2a due to handling resulted in partial destruction of IGBT gate insulator oxide layer resulting in total failure under extended load, full closed circuit behavior, rectified by addition of gate protection zener.  
  
Unanticipated arcing from HV to LV side of coil resulted in complete destruction of IGBT gate insulator oxide layer, open circuit behaviour at collector with dead short from gate to emitter, NPN transistor got **very** hot, rectified by addition of gate protection zener.

## Production Status

-   <s>Prototype Production</s>
-   <s>Prototype Testing</s>
-   <s>Send for pilot PCB Manufacture</s>
-   Local PCB Testing
-   Kits out for testing with beta testers
-   Review & Redesign (If Needed)
-   Production!

## The Arcophone

`
<object width="640" height="385"><param name="movie" value="http://www.youtube.com/v/_WfszpzNAmw?fs=1&amp;hl=en_US"></param><param name="allowFullScreen" value="true"></param><param name="allowscriptaccess" value="always"></param><embed src="http://www.youtube.com/v/_WfszpzNAmw?fs=1&amp;hl=en_US" type="application/x-shockwave-flash" allowscriptaccess="always" allowfullscreen="true" width="640" height="385"></embed></object>
`{=html}

## Version 1.x

### Version 1.0

![](/projects/coilkit1.jpg)  
We have gotten our initial shipment of 50 PCB's and as expected, we have already found a few minor issues and elements we would like to change. The 10w 1Ω resistor is getting warmer than we would like. 20w power dissipation seems more appropriate. Additionally we have some cosmetic changes to the board that will be included in version 1.1.

| Changes for next version                            |                                                 |
|:----------------------------------------------------|-------------------------------------------------|
| Add power indicator LED                             |                                                 |
| Add signal indicator LED                            |                                                 |
| Move connections to edge of board                   | And move connection pairs closer                |
| Increase thermal load capacity of 1Ω resistor       | Most likely just double up on existing resistor |
| Move capacitor away from potentially hot components |                                                 |
| Silkscreen signal input polarity                    |                                                 |
| Screw terminal power bus connections                | For chaining coil drivers to each other         |
| Screw terminal coil connections                     |                                                 |

### Version 1.2

<img src="/projects/driver12front.jpg" width="300" /><img src="/projects/driver12back.jpg" width="300" />

| Changes for next version                                             |                                                             |
|:---------------------------------------------------------------------|-------------------------------------------------------------|
| <s>Move license silkscreen to avoid pad overrun.</s>                 |                                                             |
| <s>Centre 'Coil Driver v1.2' silkscreen text</s>                     |                                                             |
| <s>Change 5A fuse to 10A on front silkscreen.</s>                    |                                                             |
| <s>Change TTL 5v to TTL In 5v on front silkscreen.</s>               |                                                             |
| <s>Change BC546/556 transistor to BC327/337 on front silkscreen.</s> |                                                             |
| <s>Change 4700uf to 4700uF on the front silkscreen.</s>              |                                                             |
| Enlarge small resistor pads.                                         | Current pads can lift if you are rough when clipping leads. |
| Pins 6 & 7 swapped on the 555 timer.                                 | Of all the things to make a mistake on, a bloody 555 timer! |

If you are interested in acquiring a kit or being a tester, contact [Daniel](/User/atrophy) at atrophy **at** artifactory **dot** org **dot** au.
