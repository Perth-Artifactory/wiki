---
title: Operation Checklist
description: 
published: true
date: 2023-10-02T12:16:17.542Z
tags: 
editor: markdown
dateCreated: 2023-02-11T10:21:37.510Z
---

##

Checklists for operating the lasers

### Big Red

* **Check whether your material can be cut by the laser**. Refer to the [Material Advice](/tools/lasers/materials) page for specifics.
* **Set your job up in [LaserCut](/tools/lasers/lasercut)**
* **Turn the laser on using either the green power button or the shortcut button on the side of the monitor**
  * **Check that the water chiller turned on**. It's the white box to the left of the laser cutter. You can tell that it's on because the green light will be on. Don't worry about the temperature just yet.
  * **Check that the extraction system turned on**. Big Red uses a large air extractor that is connected to the back of the machine. Fumes are pulled out of the machine through slots located inside the cutting bay behind the bed. Put your hand over these slots and check for slight air movement.
* **Place your material on the bed**
  * **Make sure that your material will fit under the head**. Because Big Red's bed can move up and down it's possible for the bed to be raised to a point where your material will not fit. To lower the bed press the `Z` button to switch into vertical mode and use the down arrow. To exit vertical mode press the `Z` button again.
  * **Square your material**. The bed itself is free to slide around and cannot be relied upon to be square. The only horizontal squared surface is the gantry. (The bar that the laser head moves left and right on)
  * **If engraving ensure enough space has been left on both sides of your job**. To ensure consistent engraves Big Red adds speed up/slow down buffers on each side. Unfortunately it does not take this buffer into account when determining whether your job will fit. To account for this make sure that there is at least a 5cm gap between your engrave and the edge of the bed on the horizontal axis. Don't worry, the laser isn't firing during the buffer space.
 * **Focus the laser** 
   * Check whether the material you're cutting is hard or soft. If your material is soft (like foam, leather, fabric, toast etc) find a piece of hard material (wood/acrylic/metal) that is similar in thickness to your material and perform the following steps on the hard material instead. Once the laser is focused you can swap back to your intended material.
   * Ensure that the Z probe (the stick on the left hand side of the cutting head) is over the *centre of your desired cutting area*. Failure to position the probe directly over your material during this step has a high likelihood of damaging the machine.
   * Switch the laser into Z/vertical mode by pressing the `Z` button.
   * Place your hand over the emergency stop button. In the event that the z probe fails to register during the next step the only thing preventing damage to the machine is your reaction time pressing the emergency stop button.
   * Press the `Datum` button. The bed will rise until the sensor on the Z probe is depressed. It will then lower the bed a pre-configured amount.
   * Repeat this process when changing the thickness of the material you're cutting or when you significantly reposition your material on the bed.
  * **Check whether your design will fit on your material**. The `test` button will use the head to trace a *rectangular* bounding box. You can use this bounding box to estimate whether your design will fit. The only consequence of your design not fitting is the completeness of your final piece, the laser can safely be directed at the laser bed without issue.
    * If LaserCut is set to `absolute` mode the test button will first move the head to the corner of the design as decided by the layout within LaserCut
    * If LaserCut is set to `immediate` mode the test button will trace out your design by assuming that the head starts at the top left
    * If the laser presents a `Soft Stop` error and emits a long beep your intended cut will cause the machine to go out of bounds. This has four primary causes:
      * Your design is too big
      * The head isn't positioned close enough to the top left to accommodate the size of the design
      * There are rogue lines in LaserCut. This can be checked by dragging a selection box around your design and pressing delete. If all of the entries in the layer list fail to disappear you have rogue lines somewhere outside the confines of the bed.
      * The laser origin point has been changed. Use Laser -> Set laser origin -> `TODO` to correct. You will need to download your job again.
 * **Check the temperature on the chiller**. There is a display on the front of the chiller. It is safe to operate when the chiller is displaying 25.5C or lower. If the temperature is above this limit wait a few minutes and check again.
 * **Familiarise yourself with the location of your fire suppression equipment**. Identify your closest spray bottle, fire blanket, and fire extinguisher.
 * **Check the air assist**. Put your hand under the head to confirm that the air is flowing correctly through the head and not through a hole in the air line.
 * **Close the lid**
 * **Cut/Engrave your design**. Press `Start/Pause` and your laser job will begin. You must actively supervise the laser cutting for the duration of your job. If need be the laser can be interrupted in several ways:
   * The `Start/Pause` button will pause your job. This is good if you need to walk away from the machine. The job can be resumed by pressing the button again.
   * The `Stop` button will end the job and return the cutting head to the starting position.
   * The emergency stop will immediately shut down the laser. (but not auxillary equipment like the extractor, compressor, or chiller)
 * **Remove your material**. Remove your design and discard of any scraps created.
* **Turn the laser off using either the green power button or the shortcut button on the side of the monitor**



### Middle Red

* **Set your job up in Light Burn**
* **Turn the laser on at the wall**
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
 * **Turn off the laser cutter at the wall**

### Little Red