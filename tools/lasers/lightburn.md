---
title: LightBurn Operation Guide
description: 
published: true
date: 2024-11-23T06:38:13.621Z
tags: 
editor: markdown
dateCreated: 2024-01-03T13:39:11.882Z
---

# LightBurn Operation Guide

LightBurn is the software is used to control [Big Red](/tools/lasers/bigred) and [Middle Red](/tools/lasers/middlered).

The official documentation for LightBurn can be found [here](https://docs.lightburnsoftware.com/) if required. The [beginner UI guide](https://docs.lightburnsoftware.com/BeginnerUITour.html) would be a good place to start. However, the steps below should be sufficient for laser operators and any questions should be directed at #lasers on Slack first.


## Basic operation

* **Import your DXF/AI/SVG**: File -> Import. LightBurn can import a variety of formats but can only **open** its own project files (.lbm).
* **Check your file dimensions**: Either visually confirm that the design is the expected size relative to the bed or use the resize options at the top.
* **Assign lines to layers**: Assign the lines in your design to layers by first selecting a line (or multiple using <kbd>Ctrl</kbd> or <kbd>Shift</kbd>) and then selecting a colour from the bottom of the screen.
* **Define your layers**: Layers are configured using the box in the top right.
  * Change the drop down next to each layer to either `Line` or `Fill` as required.
  * Double click on the coloured bar next to each layer to configure speed/power.
    * Speed is measured in mm/s and has an upper limit of 200/400 on Big Red and Middle Red respectively. When engraving/filling the upper limit is 600/800 respectively. Values higher than this can be set and will be displayed on the machine but the head won't actually move any faster.
    * Power is measured in a % of 100. The minimum power you can realistically achieve on Big Red is likely to be around 10%.
    * When cutting you can set a power range using the minimum and maximum power fields. The laser will reduce the power within these parameters when slowing down to go around corners etc.
    * `Line Interval` is the distance between each line of an fill (engrave). It is not present when the selected layer is set to Line.
  * Ensure that green `Output` and `Show` toggles next to each layer are checked. (see Advanced for more details)
* **Prioritise your layers**: Drag the layers to change the cut order. Layers should be done in this order: Engraving/Etching, Internal cuts, Final cut outs. This reduces the likelihood that your material will shift during the cut.
* Adjust the `Start from` dropdown
  * `Current Position`/`User Origin` will cut your design relative to an origin point you set during job setup.
  * `Absolute coords` - Your design will wherever it is placed on the bed within LightBurn
* Download your job
  * Press `Send`
  * Press `OK` to accept the existing filename
  * If required press `Yes` to overwrite the existing file
  * If you receive `Open shapes skipped` while sending your job:
    * Select `Edit` -> `Close selected paths with tolerance`
    * Set the distance threshold to about 0.1 and hit OK.
    * Download your job again using the steps above.
    * If the problem is still not resolved use the `Show me` button within the `Open shapes skipped` error to help identify the issue.
    

You have completed the basic version of setting up a job on LightBurn.

## Advanced operation/features

> Do not alter any machine settings unless you have been trained to do so!
{.is-warning}

### Repeat specific layers

The layer field `Number of passes` can be used to control how many times a layer is repeated. The feature is particularly useful when a full cut would require running the laser below 3-5mm/s. In this instance you may be better off running particular layers twice to reduce the risk of fire.

### Repeat specific layers after a job has finished

To repeat only certain layers uncheck the green output toggle next to the layers you do not wish to cut. This is preferable to deleting the vectors directly for a few reasons but mainly because the disabled layers are still included when calculating the origin point in the User Origin and Current Position modes.

### Setting the laser origin

The nine checkboxes next to `Job Origin` can be used to control the origin corner. By default the top left of the design is used for the laser origin, this setting allows you to set any of the 9 standard origin points or a custom defined point. It's your responsibility to make sure you set the origin point back to the top left after you've finished your job so the next operator doesn't get an unpleasant surprise.

### Rotary Engraver

It's possible to engrave on the side of round material up to TODO in length and TODO in diameter. Ask a laser trainer for an induction on this attachment.