---
title: arduino_eeprom
description: 
published: true
date: 2022-10-19T11:51:20.482Z
tags: 
editor: markdown
dateCreated: 2022-10-19T08:51:56.204Z
---

![](/events/arduinouni.jpg) [workshops](/workshops)

### Arduino EEPROMs

Requirements: Arduino

Prerequisites on your Computer:

-   Install Arduino 1.00 (the release version!) - Download from [Local Mirror](http://internal/useful-software/arduino) or [Arduino.cc](http://arduino.cc/hu/Main/Software)

### Arduino EEPROMs

EEPROMs are chips that can store data even when they have no power. Your Arduino uses an EEPROM to store the program code compiled from your Arduino sketch. There's also EEPROM data storage available for your program to use, allowing it to store PERSISTENT INFORMATION that will survive even when the Arduino's power is turned off - such as settings, presets, log data, user preferences...

### Reference

-    The Arduino EEPROM library reference: <http://arduino.cc/en/Reference/EEPROM>

```{=html}
<!-- -->
```
-    Examples on Arduino (if you have teh IDE installed, these will be in your Files \| Examples \| EEPROM menu)
    -   Clearing an EEPROM: <http://arduino.cc/en/Tutorial/EEPROMClear>
    -   Reading from you EEPROM: <http://arduino.cc/en/Tutorial/EEPROMRead>
    -   Writing to your EEPROM: <http://arduino.cc/en/Tutorial/EEPROMWrite>

### Guest Lecture

Guest Presenter: Bernd Felsche - Innovative Reckoning, Perth, Western Australia

#### EEPROM Parameter Management - Data Dictionary Approach

An Arduino can be used in lots of clever projects, many of which with varying behaviour determined by several to many parameters. Storing the parameters on-chip in EEPROM means that they can be changed without recompiling the program.

This presentation will illustrate the use of a data dictionary to minimise code space requirements when there are more than a few parameters. Code snippets show the use of the data dictionary for dynamic menus in configuration mode as well as in storage and retrieval functions.

Example: ![EEPROM EXAMPLE](/workshops/arduino_eeprom-sample.tar.gz)

### Homework

-   Try writing an Arduino sketch that uses a button to switch between LED lighting patterns, and remember which pattern was selected last time you switch your Arduino on. Here are clues:
    -   You will need at least one button (to trigger LED pattern state changes), and at least 2 LEDs and appropriate resistors
    -   When a button is pressed, change which LED is lit, and store which LED is lit in the EEPROM.
    -   In your init() function, read the LED state from the EEPROM and see what value is stored there from the last time the Arduino was on, and restore that value into the display LEDs...
    -   ADVANCED: Code up Next and Previous buttons, and have a whole library of LED patterns you can scroll through. (More LEDs will be needed!)
