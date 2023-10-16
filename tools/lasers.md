---
title: Laser Cutters
description: 
published: true
date: 2023-10-16T12:40:48.098Z
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

All operators must be trained before using the machines. An operator must be watching the laser cutter at all times while it is cutting.

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

All users must be trained on the laser cutters before using them.

Training consists of two parts -

* Part 1: a session to explain how to use the laser cutter including supervised jobs done by the trainee.

* Part 2: a test to ensure the operator is safe to use the laser cutter.

A user must be trained and tested on each laser cutter separately, since they are all different in certain aspects.

### Trainers

Below is a list of trainers (Artifactory volunteers who are able to train new operators). Training can be organised by posting a message to the [\#lasers](https://perthartifactory.slack.com/archives/CB9S94S2E) channel on Slack.

| Trainer Name   | LG500 "Little" | KH7050 "Middle" | LC1290 "Big" | Availability                                            |
| -------------- | -------------- | --------------- | ------------ | ------------------------------------------------------- |
| Blake Samuels  | ✓            | ✓             | ✓          | Unavailable        |
| Beau Scott     | ✓            | ✓             | ✓          | #lasers on Slack                                        |
| Bruce Chambers | -             | -              | ✓          | #lasers on Slack                                        |
| Fletcher Boyd  | ✓            | ✓             | ✓          | General Hacking Saturdays (Confirm beforehand), #lasers on Slack           |
| Glenn Martin   | ✓            | -              | ✓          | Unavailable                                             |
| Iain Graham    | ✓            | ✓             | ✓          | Unavailable                                             |
| Johannes Chuah | -             | -              | ✓          | #lasers on Slack                                        |
| Nick Bannon    | ✓            | ✓             | ✓          | Third Tuesday of the month from 6pm (Confirm beforehand) |
| Steve Hodges   | ✓            | -              | ✓          | Unavailable                                             |
| Lewis Yip | - | - | ✓ | General Hacking Saturdays (Confirm beforehand), Metal Mondays (Confirm beforehand), #lasers on Slack |

### Operators

[Operators List](/tools/lasers/operators_list) - this is a list of the people who are trained to use each laser cutter.

## Instructions for Use

### LaserCut Software

![lasercut21.png](/tools/lasers/lasercut21.png)

The software which drives both the LG500 and LC1290 is called "LaserCut" and can be found on the desktop of the computers linked up to their respective cutting machine.

[lasercut5.3_manual_v1.6.pdf](/tools/lasers/lasercut5.3_manual_v1.6.pdf)

 It's not a fantastic piece of documentation, but may be useful.
 
 Also see [MPC6515 controller page](/docs/lasers/controller_mpc6515).

**Please don't alter any of the machine settings without checking with a trainer first!**

### File Format

The LaserCut software accepts only **DXF** (Drawing eXchange Format) Files.

Which can be created using most CAD programs out there, The most commonly used ones at the Artifactory are Inkscape and Aspire which are installed on most machines in the space.

### Relative or Absolute Positioning

![immediate_check_lcp.png](/tools/lasers/immediate_check_lcp.png)

The machines can operate in either absolute positioning mode (The machine will cut the vectors in the position they are located on the outline of the bed in the software) or in relative positioning mode (The machine will cut the vectors starting at the current location of the cutting head).  
  
For most jobs it is easier to operate in *relative* positioning mode as it allows you to manually reposition the cut much faster by simply jogging the head. Absolute positioning mode is however preferable if you are using a jig to cut or engrave multiple parts. To switch between cutting modes you simply need to toggle the **Immediate** checkbox, if the checkbox is checked then the machine is operating in *relative* positioning mode, if it is not then the machine is operating in *absolute* positioning mode.  
  
**Note:** You will need to re-download your job after changing the positioning setting in order for it to take effect.

### Rules

* You cannot look at multiple laser cutters at the same time, this means you cannot operate multiple lasers at the same time.
* Clean up the bed after you are done cutting.
* Closed footwear must be worn at all times in the laser area.
* Do not attempt to open covers or fix issues yourself if you are not qualified to do so. Let #lazers on Slack know.
* Do not slam or force the main door.
* Do not leave the laser cutter while it's running.
* Only use approved materials.
* If you aren't confident performing a particular cut/setup ask for help.
* Remember you're in a shared workspace. This means that:
  * If you have a job that will take an hour and someone else has a 5 minute cut let them go ahead of you.
  * If you NEED to do big 1Hr+ jobs, Try come in at times when the space is less busy.
  * If you change the laser origin change it back when you're done. (Advanced use)
  * Clean up material left around the laser cutters.

### Tips

Pointers and helpful Tips for using the Artifactory Laser Cutters:

* **Corner power on cuts** - For most tasks "corner power" should be set to the same power as that you wish to use for the cut. However, please check this when you're setting up the power settings as a lower power setting here can be the difference between a good cut and a failure. The moving laser head moves fastest in a straight line and can "blow holes" through the corners as it slows down.
* **Don't use red in your drawings** - when you go to load the drawing to cut with lasers, the lines are highlighted red. If you use red you won't be able to tell between your red lines and highlighted lines.
* **Cut from the inside out** - when cutting intricate shapes with holes in the middle, make the inner cuts first. Define a specific layer and move the layer to the top of the operations queue. The material can move, drop or blow around after being cut free.
* **Engrave before cutting** - similar to the above. Engrave items before they have a chance to move
* You can **etch rather than engrave** by using the cut setting with a power level which marks rather than cutting through the material. eg with MDF (any thickness) on the small cutter: try 100% power, 70mm/s speed and 25% corners.
* The **large LC1290 laser** cuts faster and has a longer focus with a deeper cutting area, but may not be able to be fine enough for some engraving jobs.
* The **small LG500 laser** has a shorter focus which works well for fine engraving and thin&intricate cuts. It may not be able to cut all materials that the larger cutter can eat.
* The main software used to create laser cuts are **Aspire** and **LibreCAD**. They are installed on each computer. Any design software that exports DXFs can be used but if you're having trouble getting your files to import correctly run your design through one of these programs.

### Banned Materials

Some materials are dangerous to put in the laser cutter. If you are not sure what a material is then do not cut it. Some plastics look like acrylic but release chlorine gas when cut. Experience laser operators and maintainers can test samples of materials with extreme caution.

Forbidden Materials:

* Polycarbonates - Releases cyanide - very dangerous to people
* PVC or Vinyl - Releases chlorine gas - very dangerous to people and very bad for machine
* Glass - you can etch it but if you try to cut it will shatter.
