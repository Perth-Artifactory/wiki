---
title: vendingmachine
description: 
published: true
date: 2024-10-16T10:52:05.113Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:57:38.590Z
---

> This project page is out of date and does not reflect the current state of the vending machine. (It now works)
{.is-info}

# Vending Machine

The vending machine project has been sitting around for quite some time. Penny has taken this over as of late 2023.

## The current status

The vending machine has a working cooler, power supply, and vending motors, but the controller circuitry is not working and the coin slots weren't either. 

The machine works by running a motor that rotates and drops cans from the machine onto a metal chute, which has a piezoelectric sensor attached that detects the drop. Buttons on the front panel select which can to dispense.

## The plan

The plan is to have the machine dispense drinks based on member's RFID or NFC tags. The machine will connect to the member info database to check their preferred drink, authorise dispensing, and notify when something is dispensed. 

All the dispensing needs to happen on the machine, rather than controlled remotely over WiFi as that wouldn't be reliable enough.

High-level there's a number of subcomponents connected to a microcontroller. The plan is to use an ESP32, plus connect things via i2c.

## Sub-projects

### Processor

Lead: Penny

WiFi connection and logic will run on an ESP32, running ESPHome. I will solder a dev board onto some track board with some i2c connectors, a serial connector, and some extra pin-outs for sensors etc.

### Relay controller PCB

Lead: Penny

I have designed a custom PCB motor controller. This uses an i2c multiplexer chip and has space for 10 solid state relays, plus a bunch of GPIOs that can also be used to drive LEDs or detect button presses. It also regulates 240V down to 5V DC. This PCB will be able to be re-used for other projects.

Since some of this is going to be mains voltage, it will be inside its own enclosure for protection.

### Front panel and RFID reader

Project Lead: Ben

Ben and I have removed the existing front panel. The plan is to replace this with something probably 3D printed or laser cut with a display panel and mount the card reader. I have got an NFC/RFID reader that works with multiple different cards, which I've given to Ben to use in the design.

### Programming

Lead: Penny

This will be coded up in ESPHome. I have used this for several other projects and it's quite straighforward, allowing future maintainance and extension.


### Buttons

Currently the machine uses microswitches for each button press, and there's no illumination of each button.

The plan would be to add some lighting to this, and illuminate whichever drink type is requested (or read from the database). The buttons and lights would be run using a button mesh type of arrangement, rather than have a GPIO for each button.

### Can fill sensors

This is a stretch goal, won't be in the initial project. The longer term plan is to put sensors, possibly ultrasonic or IR time of flight, that will detect how full each slot is, allowing automated alerts to be sent for intervention when needed.

### Artifactory API

Would need to connect to an API to validate people's RFID / NFC tags, find their preferred drink, and potentially charge their account.


## Re-use potential

The relay controller will likely be re-usable for other projects. It would be great if the end result of this project is something that can be used to use specific machines in the space, especially when it's a pay per use situation.


