---
title: LaserCut Operation Guide
description: 
published: true
date: 2024-01-04T10:05:46.338Z
tags: lasers
editor: markdown
dateCreated: 2023-01-28T05:57:04.060Z
---

# LaserCut Operation Guide

> LaserCut is not used by any machine currently in use at the Artifactory. This page has been kept as a reference only.
{.is-warning}


LaserCut is the software previously used to control [Big Red](/tools/lasers/bigred) and [Little Red](/tools/lasers/littlered).

The official [manual for LaserCut](/tools/lasers/lasercut5.3_manual_v1.6.pdf) is available for reference.



## Basic operation

* **Import your DXF**: File -> Import. LaserCut can import a variety of formats but can only **open** its own project files (.ecp).
* **Check your file dimensions**: Either visually confirm that the design is the expected size relative to the bed or use the resize button on the left.
* **Assign lines to layers**: Assign the lines in your design to layers by first selecting a line (or multiple using ctrl/shift) and then selecting a colour from the bottom of the screen. We recommend not using red as it is difficult to distinguish between a red line and a selected line. (see Advanced for more details)
* **Define your layers**: Layers are configured using the box in the top right.
  * Change the drop down next to each layer to either `Cut` or `Engrave` as required. Cut draws a line, engrave fills an area.
  * Double click on the coloured bar next to each layer to configure speed/power.
    * Speed is measured in mm/s and has an upper limit of 200/400 on Big Red and Little Red respectively. Set the corner speed to the same value. (see Advanced for more details). When **engraving** the upper limit for Big Red is 600mm/s.
    * Power is measured in a % of 100. The minimum power you can realistically achieve on Big Red is likely to be around 20%.
    * Scan gap is the distance between each line of an engrave. It is not present when the selected layer is set to Cut.
  * Ensure that blue checkbox next to each layer is checked. (see Advanced for more details)
  * Ensure that the text field next to each layer is set to 1. You may need to scroll the layer window to the right to see this field. (see Advanced for more details)
* **Prioritise your layers**: Select a layer and use the up and down buttons on the screen to change the cut order. Layers should be done in this order: Engraving/Etching, Internal cuts, Final cut outs. This reduces the likelihood that your material will shift during the cut.
* Select or deselect `Immediate` as required.
  * Immediate mode will cut your design relative to the position of the head when you press start. (top left) (see Advanced for more details)
  * Absolute (unchecked immediate) mode will cut your design wherever it is placed on the bed.
* Download your job
  * Press `Download`
  * Press `Delete All`
  * Press `Download Current`
  * If you receive `engrave polyline must be closed`:
    * Close the download/transfer window
    * Select Tools -> Unite lines (see Advanced for more details)
    * Set the value to 0.1 and hit OK.
    * Download your job again using the steps above.
    * If the error persists try using Laser -> simulate to help find the stray lines.

You have completed the basic version of setting up a job on LaserCut.

## Advanced operation/features

> Do not alter any machine settings unless you have been trained to do so!
{.is-warning}

### Repeat specific layers

To the right of each layer definition is a text field (`1` by default). This defines the number of times a particular layer will be cut. The feature is particularily useful when a full cut would require running the laser below 3-5mm/s. In this instance you may be better off running particular layers twice to reduce the risk of fire.

### Repeat specific layers after a job has finished

To repeat only certain layers uncheck the checkbox next to the layers you do not wish to cut. This is preferrable to deleting the vectors directly for a few reasons but mainly because the disabled layers are still included when calculating the origin point for immediate mode.

### Setting the laser origin

Open the laser origin window by selecting Laser -> Set Laser Origin. By default the top left of the design is used for the laser origin, this window allows you to set any of the 9 standard origin points or a custom defined point. It's your responsibility to make sure you set the origin point back to the top left after you've finished your job so the next operator doesn't get an unpleasant surprise.

### Rotary Engraver

It's possible to engrave on the side of round material up to XXmm in length and XXmm in diameter. Ask a laser trainer for an induction on this attachment.