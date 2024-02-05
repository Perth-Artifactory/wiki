---
title: Laser Operation Checklist
description: How to use our laser cutters (Big Red and Middle Red)
published: true
date: 2024-02-05T14:41:47.623Z
tags: official
editor: markdown
dateCreated: 2023-02-11T10:21:37.510Z
---

> You need to be trained (and pass a test) before using our laser cutters.
>
> Only current, authorized [laser trainers](/tools/lasers#trainers) can deliver laser training.
{.is-warning}

## Big Red

* **Check whether your material can be cut by the laser**. Refer to the [Material Advice](/tools/lasers/materials) page for specifics.
* **Check whether the laser bed is unobstructed**. Ensure the bed is free of material/weights/magnets etc. When you turn the laser on the head will first move back to the top right and then to where the last user set the origin.
* **Turn the laser on** using either the green power button or the shortcut button on the side of the monitor.
  * **Check that the water chiller turned on**. It's the white box to the left of the laser cutter. You can tell that it's on because the green light will be on. Don't worry about the temperature just yet.
  * **Check that the extraction system turned on**. Big Red uses a large air extractor that is connected to the back of the machine. Fumes are pulled out of the machine through slots located inside the cutting bay behind the bed. Put your hand over these slots and check for slight air movement.
* **Set your job up in [LightBurn](/tools/lasers/lightburn)**
* **Place your material on the bed**
  * **Make sure that your material will fit under the head**. Because Big Red's bed can move up and down it's possible for the bed to be raised to a point where your material will not fit. To lower the bed press the `Z/U` button to open the menu and hold the **right arrow** until the bed is low enough.
  * **Square your material**. The bed itself is free to slide around and cannot be relied upon to be square. The only horizontal squared surface is the gantry. (The bar that the laser head moves left and right on) An easy way to align material is to use the shadow cast by the gantry when it's over your material.
  * **If engraving ensure enough space has been left on both sides of your job**. To ensure consistent engraves Big Red adds ~30mm speed up/slow down buffers on each side of any engrave. If you haven't left enough space the controller will error with `No enough extend space`. ^(sic)^
* **Focus the laser** 
   * Check whether the material you're cutting is hard or soft. If your material is soft (like foam, leather, fabric, toast etc) find a piece of hard material (wood/acrylic/metal) that is similar in thickness to your material and perform the following steps on the hard material instead. Once the laser is focused you can swap back to your intended material.
   * Ensure that the Z probe (the stick on the left hand side of the cutting head) is over the *centre of your desired cutting area*. Failure to position the probe directly over your material during this step has a high likelihood of damaging the machine.
   * Open the menu by pressing the Z/U button
   * Navigate to the `Auto focus` menu item using the **up** or **down** arrow keys. (Last menu item in the first column)
   * :warning: **Place your hand over the emergency stop button**. In the event that the z probe fails to register during the next step the only thing preventing damage to the machine is your reaction time pressing the emergency stop button.
   * Press the `Enter` button. The bed will rise until the sensor on the Z probe is depressed. It will then lower the bed a pre-configured amount.
   * Repeat this process when changing the thickness of the material you're cutting or when you significantly reposition your material on the bed.
* **Set the job origin**. If your job is set to start from either `User Origin` or `Current Position` you now need to position your design on your material. Move the head so that the red dot is at the **top left** of your material and press the `Origin` button. When your job starting position is set to `Absolute Coords` this step can be ignored.
* **Check whether your design will fit on your material**. The `Frame` button will use the head to trace a *rectangular* bounding box. You can use this bounding box to estimate whether your design will fit. The only consequence of your design not fitting is the completeness of your final piece, the laser can safely be directed at the laser bed without issue.
    * If the laser presents a `X Slop over` or `Y Slop over` error your intended cut will cause the machine to go out of bounds in the specified direction. This has four primary causes:
      * Your design is too big
      * The head isn't positioned close enough to the top left to accommodate the size of the design
      * There are rogue lines in LightBurn. This can be checked by dragging a selection box around your design and pressing delete. If all of the entries in the layer list fail to disappear you have rogue lines somewhere outside the confines of the bed.
      * The laser origin point has been changed. The `Job Origin` setting can be used to change the origin back.
 * **Check the temperature on the chiller**. There is a display on the front of the chiller. It is safe to operate when the chiller is displaying 26C or lower. If the temperature is above this limit wait a few minutes and check again.
 * **Familiarise yourself with the location of your fire suppression equipment**. Identify your closest water spray bottle, fire blanket, and fire extinguisher.
 * **Check the air assist**. Put your hand under the head to confirm that the air is flowing correctly through the head and not through a hole in the air line.
 * **Close the lid**
 * **Cut/Engrave your design**. Press `Start-Pause` and your laser job will begin. You must actively supervise the laser cutting for the duration of your job. If need be the laser can be interrupted in several ways:
   * The `Start-Pause` button will pause your job. This is good if you need to walk away from the machine. The job can be resumed by pressing the button again.
   * While the job is paused with the `Start-Pause` button it can be ended by pressing `Esc`
   * The emergency stop will immediately shut down the laser. (but not auxillary equipment like the extractor, compressor, or chiller)
 * **Remove your material**. Remove your design and discard of any scraps created.
* **Turn the laser off** using either the green power button or the shortcut button on the side of the monitor.
* **Pay for your job** using the bank details on the wall.



## Middle Red

* **Set your job up in Light Burn**
* **Turn the laser on** using the green power button.
  * **Check that the water chiller turned on**. It's the white box behind the laser cutter. You can tell that it's on because the green light will be on. Don't worry about the temperature just yet.
  * **Check that the extraction system turned on**. Middle Red uses a large air extractor that is connected to the left side of the machine. Fumes are pulled out of the machine through a slot located inside the cutting bay to the left of the bed. Put your hand over this slot and check for slight air movement.
* **Place your material on the bed**
  * **Make sure that your material will fit under the head**. Because Middle Red's bed can move up and down it's possible for the bed to be raised to a point where your material will not fit. To lower the bed press the `Z/U` button to open the menu. The first option is `TODO` and can be adjusted using the left and right arrow keys. To exit the menu press `TODO`.
  * **Square your material**. While the bed is fixed in place it is not necessarily square. The only horizontal squared surface is the gantry. (The bar that the laser head moves left and right on)
  * **Check whether your design will fit on your material**. The `frame` button will use the head to trace a *rectangular* bounding box. You can use this bounding box to estimate whether your design will fit. The only consequence of your design not fitting is the completeness of your final piece, the laser can safely be directed at the laser bed without issue.
    * If Light Burn is set to `TODO` mode the frame button will first move the head to the corner of the design as decided by the layout within Light Burn
    * If Light Burn is set to `TODO` mode the test button will trace out your design by aligning it with a user set origin point. You can change this origin point using the origin button.
 * **Focus the laser**
   * Check whether the material you're cutting is hard or soft. If your material is soft (like foam, leather, fabric, toast etc) find a piece of hard material (wood/acrylic/metal) that is similar in thickness to your material and perform the following steps on the hard material instead. Once the laser is focused you can swap back to your intended material.
   * Ensure that the Z probe (the stick on the left hand side of the cutting head) is over the *center of your desired cutting area*. Failure to position the probe directly over your material during this step has a high likelihood of damaging the machine.
   * Open the menu by pressing the `Z/U` button.
   * Navigate to the menu item `TODO`, it will be the last option in the first column.
   * Place your hand over the emergency stop button. In the event that the z probe fails to register during the next step the only thing preventing damage to the machine is your reaction time pressing the emergency stop button.
   * Press the `TODO` button. The bed will rise until the sensor on the Z probe is depressed. It will then lower the bed a pre-configured amount.
   * Repeat this process when changing the thickness of the material you're cutting or when you significantly reposition your material on the bed.
 * **Check the temperature on the chiller**. There is a display on the front of the chiller. It is safe to operate when the chiller is displaying 25.5C or lower. If the temperature is above this limit wait a few minutes and check again.
 * **Familiarise yourself with the location of your fire suppression equipment**. Identify your closest spray bottle, fire blanket, and fire extinguisher.
 * **Check the air assist**. Put your hand under the head to confirm that the air is flowing correctly through the head and not through a hole in the air line.
 * **Close the lid**
 * **Cut/Engrave your design**. Press `TODO` and your laser job will begin. You must actively supervise the laser cutting for the duration of your job. If need be the laser can be interrupted in several ways:
   * The `TODO` button will pause your job. This is good if you need to walk away from the machine. The job can be resumed by pressing the button again.
   * The `TODO` button will end the job and return the cutting head to the starting position.
   * The emergency stop will immediately shut down the laser.
 * **Remove your material**. Remove your design and discard of any scraps created.
* **Turn the laser off** using the green power button.

## What do I do if...

### The z probe makes contact with the bed during a focus/datum

> Carefully read this section in its entirety before doing anything. If at any point during these steps you are not completely sure of what to do, **stop** and ask for help on Slack rather than guessing.
{.is-danger}

These instructions assume that you pressed the emergency stop button.

* Do not turn the machine back on until the path back to the top right is free from obstructions in X, Y, and Z.
* Check if there's someone more experienced with laser cutters in the workshop at the time. Don't be afraid to ask for help.
* Check whether the lens tube at the bottom of the head has depth to spare. If it does:
  * Move the lens assembly up by loosening the brass screw on the right side of the head (above the air hose). Do not confuse this knob with the knobs on the top of the head that adjust the mirror.
  * If this has moved the head up enough to clear the bed:
    * Tighten the brass knob.
    * Manually move the head back to the top right. Push the head all the way to the right then push the gantry all the way back.
    * Turn the machine back on.
    * Lower the bed by 5-10cm.
    * Move the head to a position that makes it easy to work on.
    * Undo the brass knob.
    * Lower the lens assemble by 20mm.
    * Tighten the brassh knob.
    * Inspect the head and probe assembly for damage and report to Slack.
    * If no damage is visible you should be safe to use the machine again.
  * If the head/probe is still not clear then report the issue to #lasers on Slack and place an out of order sign on the lid of the machine. Out of order signs can be found on the shelf behind Big Red's PC.


### A piece drops down into the machine

* If it's a small piece (20mm-20mm or less) and you don't care about it, don't worry about it. It'll be removed during a laser maintenance session.
* Check if there's a laser maintainer or committee member in the space. They can retrieve the piece for you.
* If no one is around to help contact #lasers on Slack.

### The bed is visibly tilted

* Report to #lasers on Slack.