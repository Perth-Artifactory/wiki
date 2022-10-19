---
title: vendo
description: 
published: true
date: 2022-10-19T10:15:15.559Z
tags: 
editor: markdown
dateCreated: 2022-10-17T17:09:20.317Z
---

The Vendo Documentation Half way there

Part 1 - The Motors

The motors Positive lines are controlled using lines A B C D E F G

These are marked on 7 Cables going into the relay board. The common pins are all tied together using Tracks on the back of the board

So when the relay latches, It sends +18V down the line to the motor

The Relays are on Analog 0 to 7

The Negative lines are controlled from an Arduino, There are 10 Control lines, Each labelled 1-10

There are 10 IRF540 Mosfets on a PCB, This PCB has the Mosfet control lines connected to

Digital 2 3 4 5 6 7 8 9 10 11 12. The Source is connected to the -18V Side of the Power supply

Drain is connected to the Motor + Pin.

The Motors are driven in a Matrix Style array, Similar to a keypad.

There are Protection Diodes in the motors that stop Spikes.

Have a look over the Arduino Code on GitHub, it will show you how it works, As an example Sending A to the serial line

will enable Slot 1, B to do Slot 2 and so on, Lowercase letters enable more slots.

2 - USB And Power

There are 2 USB Hubs inside the vending machine, These are to make the arduinos Modular, If one breaks, Replace the arduino.

Depending on mapping of the USB devices the port numbers may change. /dev/ttyACM0 is always the LCD Screen

There are Two power supplies, One being a 24V DIN Rail, This is the motor power supply

The other being a 12/5 Dual Rail Switchmode, This provides extra +5V to the USB Lines/Hubs

The 12V side is for the LED Strip.

3 - Wiring and Specs

The NFC Reader is a standard 522 From Altronics

The RFID is a Serial Port RFID 232 Reader from Priority1Design

The LCD is a DFROBOT 128x64 LCD Screen from Altronics

The Keypad is a 12 Button Matrix Keypad from Altronics

The Relay board is a 8 Funduino Way Relay Board from Jaycar

The Mosfets are IRF540 N-Channel from Altronics

The Arduinos are standard Arduino Nano's and a Leonardo for the screen

For some reason the Leonardo was better on the screen than a nano, Nano was dim and not very bright.

The RFID Reader has a PL2303 USBtoSerial cable on it, This goes to the USB Hub and then on to the PC

The LED Strip is standard 5050 LED Strip. +12V Supply

The USB Hubs have additional Power via the +5 Rail, They tend to Brown out and drop otherwise.

4 - The Code All the code is located on GitHub under the Vending Machine project. Its up to you to understand it. I am not going to document

what each section does as by the time someone reads this it will likely be totally different.
