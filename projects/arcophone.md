---
title: Arcophone
description: 
published: true
date: 2022-10-19T12:36:09.552Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:47:01.914Z
---

# Arcophone

## Who

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Arcophone Software</th>
<th><a href="/user/skot">skot</a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Coil-Driver Boards</td>
<td><a href="/user/bdowning">bdowning</a><br />
<a href="/user/atrophy">atrophy</a></td>
</tr>
<tr class="even">
<td style="text-align: left;">Laser-cutting</td>
<td><a href="/user/zignig">zignig</a></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Solder Monkey</td>
<td><a href="/user/jmuirhead">jmuirhead</a></td>
</tr>
</tbody>
</table>

## What

The Polyplasmic Arcophone ("Arcophone" or more colloquially, "Mr Zappy") is a MIDI-controlled, 30,000V electric plasma arc instrument.

More info as this quinessential musical accessory to every mad scientist's laboratory takes shape.

## Where

The Arcophone has, in at least one of its incarnations performed at

-   Euchronia 2010
-   Australian Hackerspaces Meetup at [HSBNE](http://www.hsbne.org).
-   Spiegeltent @ Perth Fringe Festival 2011
-   Analogue to Digital 4, 6th March 2011
-   Analogue to Digital 6, 14th August 2011
-   The Harvey Lion's Nutty Professor Expo, 22nd October 2011
-   Artifactory residency @ Northbridge Piazza, April 2012

# Current status

### Hardware

-   12 voices provided by automotive ignition coils & [musicalcoildriver](musicalcoildriver) circuits
-   MIDI in optoisolator
-   Arduino Mega clone clone running our MIDI processing and spark trigger signal synthesizer software.
-   One ATX power supply

### Software

-   MIDI control via Arduino - Note on and off only at present, MIDI note stack, Voice allocation heat-load distribution algorithm
-   Custom polyphonic digital pin oscillator (because arduino's tone function is mono! boo!)
-   Variable duty cycle (to strike the arc on higher notes)
-   Pitch bend
-   Vibrato

# To Do

### Hardware

-   Proper antennae for the arcs!

As someone dropped the Arcophone, the case is much worse for wear. Christopher Hall and John Parker are designing a new one involving glass sounding boards also known as "Test Tubes". Current CorelDraw 16 files here:![](/projects/arcphone/arcophoneboard.zip)

### Software

-   Voice stacking + detune
-   Choreographed voice allocation modes, selectable by MIDI CC.
-   Frequency dependent duty cycle (to help charge the coils for the higher spark rates)
-   Velocity sensitivity by recruiting extra coils for notes
-   Mod wheel support

# Video and Photographic Evidence

`
<iframe width="560" height="315" src="http://www.youtube.com/embed/_WfszpzNAmw" frameborder="0" allowfullscreen></iframe>
<iframe width="420" height="315" src="http://www.youtube.com/embed/36xI4kt8HiU" frameborder="0" allowfullscreen></iframe>
`{=html}

20th October 2010:

<img src="/projects/arcophone_maria1.jpg" width="300" height="400" alt="arcophone_maria1.jpg" /> <img src="/projects/arcophone_coildriverarray.jpg" width="300" height="400" alt="arcophone_coildriverarray.jpg" />
