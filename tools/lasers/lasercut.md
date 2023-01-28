---
title: LaserCut Operation Guide
description: 
published: true
date: 2023-01-28T06:03:33.195Z
tags: lasers
editor: markdown
dateCreated: 2023-01-28T05:57:04.060Z
---

# LaserCut Operation Guide

The LaserCut software is used to control [Big Red](/tools/lasers/bigred) and [Little Red](/tools/lasers/littlered).

The official [manual for LaserCut](/tools/lasers/lasercut5.3_manual_v1.6.pdf) is available for reference.



## Basic operation

* **Import your DXF**: File -> Import
* **Check your file dimensions**: Either visually confirm that the design is the expected size relative to the bed or use the `TODO` button on the left.
* **Assign lines to layers**: Assign the lines in your design to layers by first selecting a line (or multiple using ctrl/shift) and then selecting a colour from the bottom of the screen. We recommend not using red as it is difficult to distinguish between a red line and a selected line. (see Advanced for more details)
* **Define your layers**: Layers are configured using the box in the top right.
  * Change the drop down next to each layer to either `Cut` or `Engrave` as required. Cut draws a line, engrave fills an area.
  * Double click on the coloured bar next to each layer to configure speed/power.
    * Speed is measured in mm/s and has an upper limit of 200/400 on Big Red and Little Red respectively. Set the corner speed to the same value. (see Advanced for more details). When **engraving** the upper limit for Big Red is 600mm/s.
    * Power is measured in a % of 100. The minimum power you can realistically achieve on Big Red is likely to be around 20%.
    * Scan gap is the distance between each line of an engrave. It is not present when the selected layer is set to Cut.
  * Ensure that `TODO` is checked for each layer (see Advanced for more details)
  * Ensure that `TODO` is set to 1 for each layer (see Advanced for more details)
* **Prioritise your layers**: Select a layer and use the up and down buttons on the screen to change the cut order. Layers should be done in this order: Engraving/Etching, Internal cuts, Final cut outs. This reduces the likelihood that your material will shift during the cut.
* Select or deselect `Immediate` as required.
  * Immediate mode will cut your design relative to the position of the head when you press start. (top left) (see Advanced for more details)
  * Absolute (unchecked immediate) mode will cut your design wherever it is placed on the bed.
* Download your job
  * Press `Download`
  * Press `Delete All`
  * Press `Download Current`
  * If you receive `TODO`:
    * Close the download/transfer window
    * Select Tools -> Unite lines (see Advanced for more details)
    * Set the value to 0.1 and hit OK.
    * Download your job again using the steps above.

You have completed the basic version of setting up a job on LaserCut.

## Advanced operation/features

> Do not alter any machine settings unless you have been trained to do so!
{.is-warning}


> TODO
{.is-warning}
