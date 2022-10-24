---
title: Basic Arduino Beginners Kit - Resources
description: 
published: true
date: 2022-10-19T11:44:06.023Z
tags: 
editor: markdown
dateCreated: 2022-10-17T17:09:29.221Z
---

# Basic Arduino Beginners Kit - Resources

## Kit Documentation

Copies of the information sheets included in kit V1.0:  
![2 x Parts sheets](/arduino_basic_starter/parts_sheets.doc)  
![Contents description sheets](/arduino_basic_starter/starter_kit_v1_2.doc)  
  
Copies of the information sheets included in kit V2.0:  
(in production)  

## Arduino Programming Environment "help" tab

As a beginner, this should be your "go to" place for information about the device and how to use it.  
While a lot of the basic language and library information is included in the download, some of the links are to the main [Arduino website](https://www.arduino.cc/).

It's a really good idea to explore the Arduino Help menus, especially the **Environment** and **Reference** sections.

**Getting Started** and **Environment** cover the software installation, loading your first "sketch" to your Arduino and the basic functions available in the programming environment.

**Reference** has several tabs. The most useful are *<u>Language</u>* which has descriptions and instructions for use of all the core programming commands of the Arduino language and *<u>Libraries</u>* which covers the core code libraries that are included with the Arduino download and links to a huge number of user contributed code libraries that can be downloaded as needed.  
  

## Arduino Website

<https://www.arduino.cc/>

A huge amount of information can be found here - although some of it is a little difficult to locate.

**Learning** \>\> **Examples** (<http://arduino.cc/en/Tutorial/HomePage>) has tutorials on each of the sketches included in the *<u>Examples</u>* tab of the Arduino programming environment.  
This is a really good place to start for learning basic circuit wiring and programming structure.  
**<u>Your kit contains all the components required to run each of these example programs.</u>**

**Learning** \>\> **Reference** is the on-line version of the same page included in the *<u>Help</u>* tab.

**Learning** \>\> **Playground** (<http://playground.arduino.cc/>) is a fantastic resource.  
Particularly useful for beginners are:  
[Manuals And Curriculum](http://playground.arduino.cc/Main/ManualsAndCurriculum)  
[Interfacing with Hardware](http://playground.arduino.cc/Main/InterfacingWithHardware)  
[User Code Library / Code Library and Tutorials](http://playground.arduino.cc/Main/GeneralCodeLibrary)  
There is also information on [interfacing with other software](http://playground.arduino.cc/Main/InterfacingWithSoftware), [finding electronic components](http://playground.arduino.cc/Main/Resources), and [some links to electronic technique tutorials, etc](http://playground.arduino.cc/Main/ElectroInfoResources).  

The **forum** <http://forum.arduino.cc/> is huge, difficult for a beginner to navigate and a bit hit-and-miss.  
Searching the forum with "\<*component you are working with*\> \<*symptom of your problem*\>" will often bring you to a forum topic which is at least tangentially related your problem. Replies to posts can often be sporadic, rude or incomprehensible to the beginner.  
Note that because Arduino is now such a ubiquitous platform, simply using Google with the search term "\<*component you are working with*\> \<*symptom of your problem*\> Arduino" will often get you the answer you need on the first page of results.  

## Basic Manuals

[Arduino Programming Notebook](http://playground.arduino.cc/uploads/Main/arduino_notebook_v1-1.pdf) by Brian Evans is linked on the Arduino *Manuals and Curriculum* page. This is an easy to follow, simple introduction to some basic circuits and Arduino code commands, although some knowledge of electronic schematic symbols is assumed. The diagrams on the Parts sheets included with your kit are modifications of some of those in this booklet.  

[Earthshine Design Arduino Starter Kit Manual](http://math.hws.edu/vaughn/cpsc/226/docs/askmanual.pdf) by Mike McRoberts ([also available here](https://archive.org/details/ArduinoStarterKitManual)) is a very good starter guide that leads up to reasonably advanced concepts like multiplexing. Your kit includes enough components to create most of the circuits in this guide, but not all.  

[Adafruit's Arduino Tutorials](http://www.ladyada.net/learn/arduino/index.html) have not been updated for ages, but they are still a good starting point. See below for more on Adafruit Industries.  

[SparkFun Inventor's Kit Guidebook](https://www.sparkfun.com/products/retired/11581). Sparkfun is a good source of electronic components and kits for the beginner. This is the guide book to one of there kits. It is available as a free .pdf download and there is a link to download all of the code examples covered in the guide.  
This is a good, very basic starter text for anybody with no electronics knowledge at all. Note that once again, your kit contains the parts required to complete most of the circuits in the book but not all of them.  
  

## Code Snippets

#### Servo

This sketch is a more functional version of the example "sweep" code included in the Arduino download and found under "Servo" in the examples menu. The servo will move to what ever angle is entered in the Serial Monitor.  
Unzip into the Arduino folder:  
![](/arduino_basic_starter/servo_serial_command.zip)  

#### Ultrasonic Sensor

This sketch is a modification of the example "ping" code included in the Arduino download and found under "06.Sensors" in the examples menu. The standard example is for an ultrasonic sensor with 3 pins. This code includes minor modifications in order to use the 4 pin sensor supplied in your kit. You may find it useful to compare this to the original.  
Unzip into the Arduino folder:  
![](/arduino_basic_starter/ping_4pin.zip)  
  

## Kit V2.0 project

#### Parking sensor / distance measurer: CODE

This sketch uses an ultrasonic sensor to indicate distance to an object using a row of LEDs. When very close to an object, a hobby servo will wave frantically.  
Unzip into the Arduino folder:  
![](/arduino_basic_starter/Parking_sensor_V02.zip)  

#### Parking sensor / distance measurer: CIRCUIT

Breadboard wiring diagram for this project  
(in production)  
===== Other Resources =====

#### TIPS FOR POSTING ON FORUMS

Maybe you have never done it before. Chances are that if stick with Arduino, electronics or programming for any length of time, you are going to and it would probably help to know the etiquette. Even if you have, perhaps you might like to have a look at the following links for some suggestions. Remember:

-   search the forum for your topic - the answer could already be there.
-   don't post to old topics - it's usually considered annoying.
-   learn the forum social rules - lurk before you post!

[Even posting in forums requires etiquette](http://www.pythian.com/blog/even-posting-in-forums-requires-etiquette/)  

#### VENDORS AND RETAILERS

[Adafruit Industries](https://www.adafruit.com/) is a fantastic source of components and pre-built or self-assembly Arduino "shields". They have extremely good documentation, tutorials, code libraries and example code for all of their products. They also have a lot of basic electronics technique tutorials.

Requests for assistance with <u>Adafruit products</u> posted to their forum are generally addressed fairly promptly - often by a staff member who actually helped develop the product.  
As with all such forums, it is intended for customers who have actually brought one of Adafruit's products. Try to make sure that the problem you are experiencing is actually related to the product by double (and triple) checking your code and wiring. Search for an existing thread that seems to be related to your problem before starting a new one. Check the FAQ's for the product first. Chances are you are not the first one to run into your specific difficulty.  
[Freetronics](http://www.freetronics.com.au/) is another good source for Arduino compatible clones and parts and some tutorials for the beginner.

[Sparkfun](https://www.sparkfun.com/) has a lot of interesting parts for sale. Their focus is on getting components to the hobby market in a way that can be easily used (breakout boards for tiny components, etc) but their documentation, code and libraries can be spotty and error prone. It's worth looking through all the comments on a given item, as problems are often addressed here.

[Seeed Studio](http://www.seeedstudio.com/depot/) parts are relatively inexpensive but also suffer from sometimes confusing or absent documentation. They sell a range of Arduino clones and shields. (They have a fantastic and inexpensive Printed Circuit Board manufacturing service, if you get to the point of designing your own PCBs).

[Little Bird Electronics](http://littlebirdelectronics.com.au/) is an Australian based retailer of Arduino and other electronic components from a variety of sources including Sparkfun, Adafruit and others.

[Altronics](http://www.altronics.com.au/) is a Perth based retailer that has a good range of electronic components for hobbyists. They also sell genuine Arduino boards and accessories. They are retailers only and their shop staff will generally be of little assistance in selecting components and parts.

[Jaycar](http://www.jaycar.com.au/) has a very similar range. They sell the Freetronics range of Arduino compatible boards and accessories. Like Altronics, they are retailers only and their shop staff will generally be of little assistance in selecting components and parts.

[RS Components](http://au.rs-online.com) has a huge range and high prices. They are not aimed at hobbyists and can offer little support or assistance to the beginner.

[Deal Extreme](http://www.dx.com), [Banggood](http://www.banggood.com) and [AliExpress](http://www.aliexpress.com/) are Asian based resellers that are a fantastic source of cheap parts and components, but documentation is non-existent. You will need to understand what you are buying and source documentation elsewhere. They often sell cheap, unofficial "pirate" copies of shields and components made by companies like Arduino, Freetronics, Sparkfun and Adafruit. Most of the components in your kit came from AliExpress.

#### PARTS SHEETS

Manufacturer data sheets for some of the components included in the kit.  
![](/arduino_basic_starter/74hc595_shift_register_data_sheet.pdf)  
![](/arduino_basic_starter/bc337_transistor_data_sheet.pdf)  
![](/arduino_basic_starter/sg90servo_data_sheet.pdf)  
![](/arduino_basic_starter/relay_data_sheet.pdf)  

#### RESISTOR COLOUR CODES

There are heaps of online colour code charts and calculators. They are all much the same. Google is your friend! - find one you like and download a copy.
