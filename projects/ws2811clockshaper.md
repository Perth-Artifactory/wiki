---
title: WS2811 Clock Shaper
description: 
published: true
date: 2022-10-19T12:43:32.769Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:57:56.493Z
---

# WS2811 Clock Shaper

## What's all this?

The WS2811 LED driver is really cool, especially when it's inside the LED.  
There are a lot of different ways people have thought of to drive them from the ATmega328, most of them use tuned assembly routines.  
My personal favouite is the use of logic gates to switch between two synchronised pulse-width channels with a SPI data line. [Link](http://www.instructables.com/id/My-response-to-the-WS2811-with-an-AVR-thing/?ALLSTEPS)  
That's a lot of transistors for what is not a big task. *cunning_fellow* even dismisses the hardware solution saying it should be a software problem.  
But given the ubiquity of SPI busses, a single transistor hardware solution appealed to me.  
This circuit uses three resistors, one capacitor and one NPN transistor to convert a basic 5V 800KHz SPI bus to the WS2811 signal scheme.  
Circuit diagram:  
<img src="/projects/spi-ws2811_schematic1.png" width="200" />  
I intend to use a lot of these, so I made a bunch of 9x14mm SMD boards, but through-hole on stripboard works fine.  
The boards were designed in KiCad and manufactured by [Hackvana](http://www.hackvana.com/store/).  
<img src="/projects/spi-ws2811_board_front.jpg" width="200" /> <img src="/projects/spi-ws2811_board_back.jpg" width="200" />  
The soldering is a bit messy, 0608 is harder when you have an arm in plaster.  
If people want the design files, they'll show up on Github eventually. If you're impatient, use strip-board  

## A Functional Description

The clock line passes through one resistor to the data out line, past the collector of the transistor.  
if the data-in line is high, the transistor stays off leaving the 50% duty cycle of the clock on the data out line.  
if the data-in line is low, the transistor switches on pulling the data-out line low (sinking the current to data-in), but only after the capacitor charges.  
This reduces the clock pulse to about 10% of the 800KHz period, corresponding to a zero pulse to the WS2811.  
Scope Trace:  
<img src="/projects/spi-ws2811_scope_trace.jpg" width="200" />  
The upper trace is the SPI data, the lower trace is the output line (truncated clock)  

## Pitfalls

Because the transistor is switched on by a RC circuit, the signal out is very repeatable, but a bit rounded.  
so the data-out from this circuit is not really suitable for running over long cables without a Schmitt trigger.  
**BUT** the WS2811 datasheet mentions per-chip data line amplifiers that square-up this dodgy waveform, so the signal is text-book perfect after the first LED.  
(if you're driving a LED matrix and really need a zero indexed first pixel, run SPI to the matrix and drop this board in before the first pixel. It's really small.)  
The circuit is also powered by the SPI lines, so you may need to tweak the RC values for a 3V bus.  

## Software!

If you're on Arduino, you might notice that the SPI port doesn't have an 800KHz clock divider setting.  
One of the timers does have 800KHz settings, so you could use SPI in slave mode and give up a PWM channel for your clock.  
Or you could use the UART. The ATmega UART has a much finer clock divider, and it has a master SPI mode. (clock-out at pin 4)  
I've mocked up a basic transmit-only UART MSPI mode library for the ATmega328, soon to be on Github.  
It's fully interrupt driven on the UART only, no assembly, and transmits to the WS2811 with cycles to spare outside of the interrupt routine, even on an 8MHz core.

## Related Findings

While fiddling with the clock-divider on the ATmega UART, I tried different speeds. My 800KHz WS2811 chips responded up to 900KHz and down to 200KHz.  
I suspect that this circuit could be used with the SPI settings available on the raspberry pi using MetaLab's [RetinaTattoo](https://metalab.at/wiki/RetinaTattoo)

## Pretty Pictures

The same circuit on strip-board driving a dense WS2811 LED bar, also KiCad and Hackvana.  
<img src="/projects/ws2811_32ledbar.jpg" width="200" />  
The same circuit doing POV from an ATmega328. Notice how the PWM chops greys into broken stripes.  
<img src="/projects/ws2811_nyan_pov.jpg" width="200" />  
