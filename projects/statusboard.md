---
title: statusboard
description: 
published: true
date: 2022-10-19T12:42:04.317Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:55:40.468Z
---

Grand Master plan to replace the [ABS box containing doorbot](/projects/opendoorcontrol) with something larger.

-   Move the PSU / Battery backup higher up the wall
-   Make wooden frame (to go over existing burglar alarm panel) to take ply/mdf engraved front
    -   Will also need to be clear of lightswitch on side of distribution board
    -   Needs to be over ribbon cable from external readers/led/button
    -   Needs to be able to pick up cables to door solenoid
-   LCD Display for basic status
-   Light switch (momentary push with indicator) for floodlight PSU - see below
-   Simple green / red open/close space buttons that also update spaceapi and coloured sign
-   excessive decoration / branding
-   Connects to external doorbell and RGB LED

Contraints

     * Needs to contain raspberry pi (network, power, sound) + relay board + interfaces to lock and external sensors.
     * external cabling MUST be neat.

Wishlist for mk2

     * RFID card reader behind
     * Status LEDs for various space things.
     * allow remote control / status out

Basic idea thrown to the list on <https://groups.google.com/forum/#!topic/artifactory-core/a8n6lxrAz54>

The external floods are being driven off an old HP DPS600PB Server PSU (<http://www.rcgroups.com/forums/showthread.php?t=1581061>), which not only gives us 12v at 27A (remote start via shorting several pins together) but also 5v at 7A on standby. The latter would be ideal for the [beacon of guthrie st](/projects/lightboxsign) (fed via one of the relays) and the main PSU start/stop can be done via the PsON and PsKILL to ground, also via one of the relays.

Additional logic can be added to Doorbot (<https://github.com/Perth-Artifactory/doorbot>) to turn on the coloured sign on and annouce 'space open' to spaceapi by member hitting the 'open space' button and turning floodlights off (after a delay) if dark and closing space, (perhaps flash sign?) when they hit the 'close space' button.
