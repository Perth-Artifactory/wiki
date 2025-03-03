---
title: Big Red Training Guide
description: 
published: true
date: 2023-12-12T00:27:21.782Z
tags: official, presentation
editor: markdown
dateCreated: 2023-03-24T10:18:19.068Z
---

# What to expect {data-background-image="https://artifactory.org.au/assets/site/gallery/20181123_002935.jpg"}

::: incremental
* Training is run over 2 sessions: A practical training session and an assessment conducted on a different day
* Make use of all the resources we provide you. (Checklist, operation guides etc)
:::
# Turn the machine on at the wall

## Water Chiller

It's the white box to the left of the laser cutter. You can tell that it's on because the green light will be on. Don't worry about the temperature just yet.

::: notes
Most people don't know what an industrial chiller looks like, point it out and explain why it's important.
:::

## Fume Extractor

Big Red uses a large air extractor that is connected to the back of the machine. Fumes are pulled out of the machine through slots located inside the cutting bay behind the bed. Put your hand over these slots and check for slight air movement.

::: notes
Since the primary sound generated by the extractor is in the next room it's difficult to determine by sound alone whether the extractor is connected, hence the encouragement to physically check. For a variety of reasons warn the trainee that there's going to be a residue on the slots before they touch them.
:::

# Place your material on the bed

## Movement

* Press `esc` to exit the menu
* Use the arrow keys to move the head around
* Press the Emergency Stop

::: notes
Your trainee needs to be comfortable with pressing the emergency stop, get them to press it now and show them that the head returns to the top right when the machine is powered up.
:::

## Height check

Because Big Red's bed can move up and down it's possible for the bed to be raised to a point where your material will not fit. To lower the bed press the Z button to switch into vertical mode and use the down arrow. To exit vertical mode press the Z button again.

::: notes
This is going to be their first time operating the laser so talk about why we need to use the escape button, how to tell when the controller has registered a button press, and why it's called Z.
:::

## Square your material

The bed itself is free to slide around and cannot be relied upon to be square. The only horizontal squared surface is the gantry. (The bar that the laser head moves left and right on)

::: notes
It's really easy for a trainee to focus on alignment by using the controls, remind them that they can also physically move their material as well.
:::

## Engraving space

To ensure consistent engraves Big Red adds speed up/slow down buffers on each side. Unfortunately it does not take this buffer into account when determining whether your job will fit. To account for this make sure that there is at least a 5cm gap between your engrave and the edge of the bed on the horizontal axis. Don't worry, the laser isn't firing during the buffer space.

## Check design size

The `test` button will use the head to trace a rectangular bounding box. You can use this bounding box to estimate whether your design will fit. The only consequence of your design not fitting is the completeness of your final piece, the laser can safely be directed at the laser bed without issue.

::: notes
Emphasising the rectangular nature of the test will help operators down the line when engraving round designs. Demonstrate a soft stop so that they know what it looks and sounds like.
:::

# Focusing the laser

![focus](https://mellowpine.com/wp-content/uploads/2022/04/Laser-712px-1.jpg)

## Soft material

If your material is soft (like foam, leather, fabric, toast etc) find a piece of hard material (wood/acrylic/metal) that is similar in thickness to your material and perform the following steps on the hard material instead. Once the laser is focused you can swap back to your intended material.

## Probe position

Ensure that the Z probe (the stick on the left hand side of the cutting head) is over the *centre of your desired cutting area*. Failure to position the probe directly over your material during this step has a high likelihood of damaging the machine.

## Probing

::: incremental
* Switch the laser into Z/vertical mode by pressing the Z button
* Place your hand over the emergency stop
* Press the `datum` button
:::

::: notes

For their first z-probe get your trainee to place their hand over the emergency stop but tell them that you will tell them if they need to press the button this time. It's not uncommon for trainees to overreact and press the emergency stop unnecessarily.

Make sure the trainee understands that their hand must be over the emergency stop any time they focus the laser.
:::

## When things go wrong

Unlike almost every other part of laser cutting this is the one step where mistakes have a high likelihood of damaging the machine. If the probe is caught in the bed **you cannot fix the problem yourself**. Instead contact:

::: incremental
* Maintainers in the space
* #lasers on Slack
* Blake
:::

Until you turn the machine back on it's an easy fix for maintainers.

# Fire suppression

Lasers cut by burning the material. To prevent a fire you must ensure air assist works and only cut approved materials.

##

::: incremental
* Spray bottle
* Remove the material
:::

##

::: incremental
* Fire Blanket
* Fire Extinguisher
:::

# Prep for cutting

::: incremental
* Check the temperature on the chiller. It's safe to operate when the chiller is displaying 25.5C or lower. If the temperature is above this limit wait a few minutes and check again.
* Familiarise yourself with the location of your fire suppression equipment.
* Turn on extra air assist if required
* Close the lid
:::

::: notes
Explain the three reasons we use air (protect the lens, clean the cuts, prevent fires). Since you're asking the trainee to put their hand under the head of quite a powerful machine this is also a great time to talk about machine interlocks.
:::

# Press start!

You must supervise the machine when it's running.

There's a few different ways to stop the machine:

::: incremental
* The Start/Pause button will pause your job. This is good if you need to walk away from the machine. The job can be resumed by pressing the button again.
* The Stop button will end the job and return the cutting head to the starting position.
* The emergency stop will immediately shut down the laser.
:::

::: notes
Lasers are cool as hell, give your trainee some time to watch the cool thing.
Once they've had a chance to watch the laser talk about the various ways the laser can be stopped and their consequences.
:::

# Shutdown

::: incremental
* Turn off the air assist. The laser cutters are situated close to the social and project areas. To prevent unnecessary noise pollution turn off the air assist before opening the lid of the machine.
* Remove your design and discard of any scraps created.
* Return the laser to the top right
* Turn off the machine at the wall
:::

::: notes
Talk about useful scrap sizes and that it's okay to discard the leftovers from cuts. "Yes you could do something with 100 tiny MDF ovals but unless you have a specific idea in mind it's probably better to just cut them when you need them". Discuss which scraps can remain in the bed and which can't.
:::