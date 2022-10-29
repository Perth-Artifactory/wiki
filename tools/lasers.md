---
title: Laser Cutters
description: 
published: true
date: 2022-10-27T16:04:52.267Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:57:18.915Z
---

# Laser Cutters

The Perth Artifactory has 3 laser cutters available for use. For details on each machine see these pages:

* [Big Red](/tools/lasers/bigred)
* [Middle Red](/tools/lasers/middlered)
* [Little Red](/tools/lasers/littlered)

The laser cutters use high intensity collimated infrared light to cut and engrave various materials. The most common materials cut on our laser cutters are woods and acrylic.

All operators must be trained before using the machines. An operator must be watching the laser cutter at all times while its cutting.

## Safety

The laser cutters are dangerous tools. The main hazards:

|                                                                 |      |
| --------------------------------------------------------------- | ---- |
| ![ionising_radiation.svg](/resources/hazards/fire.png)          | There is a constant risk of fire when cutting most materials. Supervise the laser at all times. |
| ![ionising_radiation.svg](/resources/hazards/crush.svg)         | There is the risk of a crush injury when raising and lowering the bed. Keep your hands out of the machine when changing the bed height or focusing the laser. |
| ![ionising_radiation.svg](/resources/hazards/laser.png)         | The lasers in these machines are capable of producing intense, collimated beams of light that can cause significant injury. Do not attempt to remove panels or bypass interlocks unless trained and authorised to do so. |
| ![ionising_radiation.svg](/resources/hazards/visible_light.svg) | When vaporised some material will release a bright light. Use your own judgement as to whether the light is too bright to look at directly. |
| ![ionising_radiation.svg](/resources/hazards/high_voltage.svg)  | The laser cutters operate at approximately 30,000V. Do not attempt to remove panels or bypass interlocks unless trained and authorised to do so. |

## Usage Costs

To cover the cost of maintenance and consumables the laser cutters have fees per minute of operation. When a laser cutter job finishes, the display shows the time it took. This is the time to be charged. The laser cutter software on the PC can give an estimate of cut time before you start a job. It tends to under estimate though especially for engraving.

![big_red_laser_time_readout.jpg](/tools/lasers/big_red_laser_time_readout.jpg)

Refer to [Tool Usage Fees](/docs/policies/fees) for the current fees.

## Training

All users must be trained on the laser cutters before using them. Training consists of two parts - first a session to explain how to use the laser cutter including supervised jobs done by the trainee. The second part is a test to ensure the operator is safe to use the laser cutter. A user must be trained and tested on each laser cutter since they are all different in certain aspects.

### Trainers

Below is a list of trainers (Artifactory volunteers who are able to train new operators). Training can be organised by posting a message to the \#lazors channel on slack.

| Trainer Name   | LG500 "Little" | KH7050 "Middle" | LC1290 "Big" | Availability                                            |
| -------------- | -------------- | --------------- | ------------ | ------------------------------------------------------- |
| Blake Samuels  | Yes            | Yes             | Yes          | Arduino U (Confirm beforehand), #lazors on Slack        |
| Beau Scott     | Yes            | Yes             | Yes          | #lazors on Slack                                        |
| Bruce Chambers | No             | No              | Yes          | #lazors on Slack                                        |
| Fletcher Boyd  | Yes            | Yes             | Yes          | General Hacking Saturdays (Confirm beforehand), #lazors on Slack           |
| Glenn Martin   | Yes            | No              | Yes          | Unavailable                                             |
| Iain Graham    | Yes            | Yes             | Yes          | Unavailable                                             |
| Johannes Chuah | No             | No              | Yes          | #lazors on Slack                                        |
| Nick Bannon    | Yes            | Yes             | Yes          | Third Tuesday of the month from 6pm (Confirm befrehand) |
| Steve Hodges   | Yes            | No              | Yes          | Unavailable                                             |


### Operators

[Operators List](/tools/lasers/operators_list) - this is a list of the people who are trained to use each laser cutter.

## Instructions for Use

### LaserCut Software

<img src="/tools/lasercutters/lasercut21.png" class="align-left" width="200" />

The software which drives both the LG500 and LC1290 is called "LaserCut" and can be found on the desktop of the computers linked up to their respective cutting machine.

<embed src="/tools/lasercutters/lasercut5.3_manual_v1.6.pdf" class="align-center" /> - It's not a fantastic piece of documentation, but may be useful. Also see [MPC6515 controller page](/docs/lasers/controller_mpc6515).

**Please don't alter any of the machine settings without checking with a trainer first!**

### File Format

The LaserCut software accepts only **DXF** (Drawing eXchange Format) Files.

Which can be created using most CAD programs out there, The most commonly used ones at the Artifactory are Inkscape and V-Carve which are installed on the CAD machines in the Design Lab which can then saved in the internal network the PC connected to the laser cutters can access.

### Relative or Absolute Positioning

<img src="/tools/lasercutters/immediate_check_lcp.png" class="align-left" width="200" /> The machines can operate in either absolute positioning mode (The machine will cut the vectors in the position they are located on the outline of the bed in the software) or in relative positioning mode (The machine will cut the vectors starting at the current location of the cutting head).  
  
For most jobs it is easier to operate in *relative* positioning mode as it allows you to manually reposition the cut much faster by simply jogging the head. Absolute positioning mode is however preferable if you are using a jig to cut or engrave multiple parts. To switch between cutting modes you simply need to toggle the **Immediate** checkbox, if the checkbox is checked then the machine is operating in *relative* positioning mode, if it is not then the machine is operating in *absolute* positioning mode.  
  
**Note:** You will need to re-download your job after changing the positioning setting in order for it to take effect.

### Tips and Tricks

Basic Laser cutter Rules and Tips:

1.   You cannot look at both laser cutters at the same time, This means you cannot operate both Little and Big Red at the same time.
2.   Clean up the bed after you are done cutting.
3.   Closed footwear must be worn at all times in the laser area, Due to the large and heavy objects in the area there is a crushing risk.
4.   Do not attempt to open covers or fix issues yourself if you are not qualified to do so. Let the list know if there is an issue so it can be safely resolved.
5.   Ensure Chiller temp is correct before operating, I have seen over the last week or two countless times where the chiller is at 30+ Degrees and people are cutting.
6.   Do not slam or force the main door, if its not closing there is probably something in the way, Move it and try again.
7.   Do not leave the laser cutter while its being used, This may result in the Pause button being pressed by someone, Or in some cases the E-STOP button pressed, If you are withing ear/eyeshot of the laser cutter this is generally considered OK (Going to the fridge etc)
8.   Non approved materials are not to be cut in the machines, I have found two cases where people are cutting(trying to cut) ABS in the last 2 weeks.
9.   If you aren't confident, Then dont do it.
10.  If you dont know... Ask.

**General Courtesy:**

1.   If you have a job that will take an Hour, But someone else has a 5 minute cut, Let them ahead of you.
2.   If you NEED to do big 1Hr+ jobs, Try come in at times when the space is less busy (At night)
3.   If you change the laser origin, Change it back when you are done, There is nothing more frustrating than downloading your design just to find the origin is changed from the last person who used it. (Yes you)
4.   Clean up after yourself, Anything, Even if it has meat left on it, Left out will be disposed off, No questions asked. (Or chopped up), Dont complain when your big bit of 3mm MDF goes missing after leaving it out.
5.   If it doesn't have a name of it, Its declared free-game, unless its obvious.

Tips:

-   Big red does not like engraving over 200 Speed, It Rattles the gantry and causes all sorts of harmonics, It is very important to not go over \~200.
-   Little Red has a laser accuracy of 0.1mm, This means that your engrave at 0.01mm will take 10x longer than a engrave at 0.1mm (And will look the same), ITs a waste of your time and money.
-   Big Red Is not designed for high detail engraving and you wont get the result like you do on Little Red.

Pointers and helpful Tips for using the Artifactory Laser Cutters:

-   **Corner power on cuts** - For most tasks "corner power" should be set to the same power as that you wish to use for the cut. However, please check this when you're setting up the power settings as a lower power setting here can be the difference between a good cut and a failure. The moving laser head moves fastest in a straight line and can "blow holes" through the corners as it slows down.
-   **Don't use red in your drawings** - when you go to load the drawing to cut with lasers, the lines are highlighted red. If you use red you won't be able to tell between your red lines and highlighted lines.
-   **Cut from the inside out** - when cutting intricate shapes with holes in the middle, make the inner cuts first. Define a specific layer and move the layer to the top of the operations queue. The material can move, drop or blow around after being cut free.
-   **Engrave before cutting** - similar to the above. Engrave items before they have a chance to move
-   You can **etch rather than engrave** by using the cut setting with a power level which marks rather than cutting through the material. eg with MDF (any thickness) on the small cutter: try 100% power, 70mm/s speed and 25% corners.

-   The **large LC1290 laser** cuts faster and has a longer focus with a deeper cutting area, but may not be able to be fine enough for some engraving jobs.

-   The **small LG500 laser** has a shorter focus which works well for fine engraving and thin&intricate cuts. It may not be able to cut all materials that the larger cutter can eat.

-   The main software used to create laser cuts are **VCarve** and **LibreCAD**. They are installed on each CAD computer.
    -   VCarve is easier to use and works better with the software on the CNC machines.
    -   LibreCAD has more features but as such is a little harder to use and often creates files that cannot be fully read by the laser cutters. It helps to open these files in VCarve and export again as DXF.
    -   VCarve runs happily within Wine (Windows emulator) on Debian.
    -   In VCarve it is also helpful to select all lines on each layer one at a time and join the lines. This allows the laser to cut lines in a continuous motion and reduces travel time for the laser. This reduces the cut time and saves you money.

### Banned Materials

Some materials are dangerous to put in the laser cutter. If you are not sure what a material is then do not cut it. Some plastics look like acrylic but release chlorine gas when cut. Experience laser operators and maintainers can test samples of materials with extreme caution.

Forbidden Materials:

-   Polycarbonates - Releases cyanide - very dangerous to people
-   PVC or Vinyl - Releases chlorine gas - very dangerous to people and very bad for machine
-   Glass - you can etch it but if you try to cut it will shatter.
