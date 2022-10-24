---
title: arduinos_and_midi
description: 
published: true
date: 2022-10-19T11:51:29.589Z
tags: 
editor: markdown
dateCreated: 2022-10-19T08:52:05.477Z
---

![](/events/arduinouni.jpg)

[workshops](/workshops)

## MIDI and Arduinos

Presenter: SKoT McDonald

Requirements: MIDI enabled computer or keyboard. MIDI cable. Arduino. MIDI breakout shield (some available for sale)

Prerequisites on your Computer:

-   Install Arduino 1.00 (the release version!) - Download from [Local Mirror](http://internal/useful-software/arduino) or [Arduino.cc](http://arduino.cc/hu/Main/Software)
-   Install the latest MIDI Library (3.2 or greater at time of writing): [Local Mirror](http://internal/useful-software/arduino/libraries/Arduino_MIDI_Library_v3.2.zip) or [Sourceforge](http://sourceforge.net/projects/arduinomidilib/files/Releases)
    -   You must unpack the MIDI library zip file into the "Arduino/Libraries/MIDI" folder.
        -   On Mac: /Users/\<you\>/Documents/Arduino/Libraries/MIDI
        -   On Windows: C:\Program Files\Arduino\Libraries\MIDI
        -   On Linux:
    -   Arduino MIDI Library Reference is <http://arduinomidilib.sourceforge.net/a00001.html>
    -   Very basic MIDI code examples are within the MIDI Library

## Lecture

### MIDI Devices Overview

     * What it is used for - controlling synthesisers, sequencers, other music devices. 
     * Similar to DMX in some ways - DMX used to control lighting and theatre effects. 
     * Examples of gadgets 
       * Keyboards
       * E-drums
       * Wind-controllers
       * Trigger pads
       * Knob banks
       * Weird sound-artist sensor-installations

### MIDI Protocol

     * Dates from 1970s - just won't die. Ubiquitous, cheap, even if doesn't cover all desired control possibilities.
     * How are MIDI messages constructed: [[http://www.midi.org/techspecs/midimessages.php]]
       * STATUS BYTE 
         * Global Messages  (eg song start/stop, MIDI Clock,...) 
         * Channel messages - command nibble, channel nibble (Examples: noteOn, noteOff, cc's,...) 
         * has high bit set - 0x80
       * DATA BYTES 
         * follow a status byte 
         * High bit NOT set on data bytes! Restricts range to [0,127]
         * e.g. Note On has note number [0,127], velocity [0,127]. 
     * Most important to know are NOTE ON, NOTE OFF and CONTINUOUS CONTROLLER messages.
     * Gotchas and things to be aware of
       * noteOn vel0 = noteOff!
       * Counting starts at zero in code land, but 1 in documentation / display to user. Musicians don't know what a 0 is.
       * Running status - if no status byte is received, use previous status byte. Best to use a MIDI library to hide this.

### MIDI Hardware

     * Circuit Specs [[http://www.midi.org/techspecs/electrispec.php]]
       * opto-isolation on MIDI In
       * MIDI Out provides ground, MIDI In does not!
     * Arduino gotchas
       * On smaller Arduinos with only one serial port, MIDI is transmitted / received over the same serial port used to program the Arduino. It also means you can't use the Serial Monitor for watching any debug messages from the Arduino on your computer. Argh. You CANNOT have a MIDI device attached at same time as re-programming your Arduino! Luckily the sparkfun MIDI breakout board has a little "program/run" switch. Make sure you switch it to "PGM" when downloading new code to your Arduino, and "RUN" when you want to use your Arduino.      

## Practical

### Exercise 1: Input: MIDI Knob Reader

     * Read a trim pot attached to analogue in and spit out MIDI CC values
     * The importance of smoothing resistor values, minimum change before sending msgs.
     * **Arduino Sketch:** {{:workshops:midi_exercise1_knob2cc.zip|}}
     * //Bonus Points Homework// 
       * Extend this to several knobs

### Exercise 2: Output: MIDI-to-Voltage

     * MIDI CC to analogue out voltage (indicator light)
     * **Arduino sketch:** {{:workshops:midi_exercise2_cc2cv.zip|}}
     * //Bonus Points Homework//
       * Extend this to several CV outs
       * Implement a 3 channel (RGB) light dimmer controlled by MIDI CCs. {{:workshops:midi_exercise2_2_cc2rgb.zip|}}

### Exercise 3: Synthesis: Tone Generator

     * MIDI Note changes freq of PWM output.
     * **Arduino sketch:** {{:workshops:midi_exercise3_synthtone.zip|}}
     * //Bonus Points Homework// 
       * Implement pitchbend {{:workshops:midi_exercise3_1_pitchbendtone.zip|}}
       * Implement a MIDI note stack (there is one in the Arcophone sketch!) 
       * Implement an arpeggiator

### Exercise 4: Synthesis: LFO Generator

     * MIDI controllable LFO rate (pitch), shape
     * Rate will change between 0.1 and 100Hz
     * Shape will change between triangle and saw
     * **Arduino Sketch:** {{:workshops:midi_exercise4_lfo.zip|}}
     * //Bonus Points Homework// 
       * Multiple LFOs

### Exercise 5: Step Sequencer

     * **Arduino Sketch**: TODO
     * DIP switch banks to set notes
     * Trim pot to set tempo 
     * LED bank of step indicator "chaser lights"
     * //Bonus Points Homework// 
       * Song Start / Song Stop response

### Exercise 6: Multiplexed Control Surface

     * How to make an 8 knob MIDI-input device using only 1 analogue input
     * Use 3 digital pins as input selection controls on an 8-way multiplexer feeding 1 analogue input, and loop quickly!
     * **Arduino sketch:**  {{:workshops:midi_exercise6_multiplexedknobs.zip|}}
     * //Bonus Points Homework//
       * Make a 64 knob surface with only 6 digital pins and a single analogue input! (Hint: use a multiplexer to multiplex 8 multiplexers...)
