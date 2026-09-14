---
title: Plasma Cutter Operation Guide
description: 
published: true
date: 2026-09-14T18:39:05.331Z
tags: 
editor: markdown
dateCreated: 2026-09-14T17:39:16.293Z
---

> You need to be trained (and pass a test) before using our CNC plasma cutter.
{.is-warning}

## Pre work

* **Check whether your material can be cut by the plasma cutter**. Only electrically conductive metals can be cut. The materials primarily supported are:
  * Aluminium \<10mm
  * Mild Steel \<12mm
  * Stainless Steel: \<10mm (Extra training required)
* **Program your job**: Use either:
  * Fusion 360 (TODO: postprocessor details)
  * Any vector program that can export DXF + FastCAM
* **Save your exported gcode** onto a USB drive, do not insert it into the controller just yet.

## Machine setup

* **Position the plasma table**. When moving the table around the workshop make sure the table is aligned so the slats act as baffles. Consider:
  * How easy it will be to shield surrounding equipment and participants with welding screens
  * Proximity to both 32A 230V and 10A 230V sources
  * Where the x axis gantry will extend when cutting on the left hand side of the table
* **Connect the cables**:
  * **Controller power**: Yellow control box to a normal outlet
  * **Plasma power**: Back of Hypertherm plasma unit to a 32A single phase outlet (e.g. Welding bay). Ensure the orange retention ring is tight.
  * **Earth lead**: Front of plasma unit to plasma table (Tab under the front left side of the gantry). Ensure the plasma side is fully rotated clockwise and both sides of the earth clamp are firmly on the table.
  * **Control and sense leads**: Back of plasma unit (single large plug) to the two yellow control box (two break-out plugs). Ensure retention rings on both sides of the cable are tight.
  * **Torch lead**: Cable permenantly attached to X axis gantry to front of plasma unit. Should click when pushed in, no rotation or locking ring required.
  * **Compressed air**: Workshop air into back of filter on the back of the plasma unit
* **Turn on the plasma unit** using the switch at the front.
* **Disengage motor control** using the metal switch above the controller screen and gently move the head so it will be well clear of material during loading.

## Material setup

* **Consider manual handling**. Material used in this machine may be unsafe for one person to move alone (weight). Consider getting another attendee to assist.
* **Position the material** near the center of the bed (reduces splashing). When cutting small parts (<150mm Y) ensure the part will be completely supported by at least two slats OR will drop cleanly into the bath.
* **Be mindful of coming into contact with the bath liquid**. If you come into contact with the bath liquid while positioning material go wash your hands in the toilet or outside sink before continuing with further steps (not the kitchen sink). Bath liquid has no *immediate* negative effect on your skin but should be washed off within several minutes. It may also stain your clothes depending on the current composition.

## Job setup

* **Insert your USB**. Inserting at this stage means you don't accidentally snap the drive off when setting up the machine.
* **Load your file**.
  * Press `F2 (Files)` -> `F2 (U Disc)`
  * Navigate the directory structure using the arrows keys and `Enter`
  * Press `F7 (Preview)` to preview the currently highlighted file
* **Manipulate your part**. Press `F3 (Part Option)`
  * **Angle**: `F2 (Angle)` -> `F2 (Input Rotation Angle)
  * **Duplicates**: `F3 (Array)` -> `Straight` or `Stagger` depending on layout requirements (reducing excess heat at corners etc)
* **Set your origin point**. (While still in the Part Option menu)
  * Press `F1 Start Point`
  * Select your desired origin
  * Press `F8 OK` then `F8` to save settings and return to home screen.
* **Raise the torch** higher than the material using `S↑`
* 




