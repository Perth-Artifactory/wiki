---
title: Big Red - Lens Cleaning Procedure
description: 
published: true
date: 2022-12-30T04:52:22.670Z
tags: lasers
editor: markdown
dateCreated: 2022-12-28T16:42:16.881Z
---

# Big Red - Lens Cleaning Procedure

> This procedure is for use by trained laser maintainers.
> Do not perform this task unless you have been specifically trained.
{.is-warning}

Laser cutters use a lens to focus a wide beam of energy down to a focused point.

The lens accumulates dirt over time (smoke etc) which reduces the cutting power of the laser.

Cleaning the lens should be done frequently in order to maintain the cutting power of the laser.

## Objectives

* Disassemble the laser head assembly to access the lens
* Clean the lens
* Reassemble the laser head assembly
* Test Z-probe and laser cutting after re-assembly.

## Laser head anatomy

![big-red-head-anatomy.jpg](/tools/lasers/big-red-head-anatomy.jpg)

## Equipment

Specialised equipment needed for this task is located in the laser maintenance toolbox.

The combination for the lock on the toolbox is given to people who have been trained in laser maintenance procedures.

You will need:

* An A4-sized piece of material to use as a working surface.
* The "laser lens wrench"
* A small phillips head screwdriver
* A spray bottle of isopropyl alcohol (IPA)
* Polishing cloths

![big-red-lens-cleaning-tools.jpg](/tools/lasers/big-red-lens-cleaning-tools.jpg)

## Procedure

1. Start the laser.

2. Evaluate the current cutting speed of the laser on 3mm MDF.
    * Use the test files `LC1290-bigred-25--50.ecp` or `LC1290-bigred-40--60.ecp` located in `\\filer\Member Work\Fletcher Boyd\Resources\Lasers\laserspeeds\`.
    * The "cut speed" of the laser corresponds to the cut rectangle that falls out immediately with no force applied.

3. Drive the laser head to the front and centre of the bed, so you can reach it easily.

![big-red-lens-cleaning-1.jpg](/tools/lasers/big-red-lens-cleaning-1.jpg)

4. Manually drive the Z-axis down to create working space underneath the laser head.

5. Put the A4 piece of material under the head. This creates a clean working surface for parts to lie on, and catches any small parts you may drop.

6. Disassemble the laser head -

    * **Loosen** (do not remove!) the two screws securing the Z-probe to the lens tube.
    * **Loosen** the thumb-screw securing the lens tube.
    * Unscrew the air assist nozzle from the lens tube.

![big-red-lens-cleaning-2.jpg](/tools/lasers/big-red-lens-cleaning-2.jpg)

9. Use the laser lens wrench to unscrew the ring which holds the lens in the lens tube. Be careful not to scratch the lens.

11. Take note of the orientation of the lens (curved side up/down) and the position of the silicon O-ring.

12. Clean the lens with copious amounts of isopropyl alcohol. Repeat until lens is as clean as possible.

13. Reassemble the lens, O-ring and locking ring back into the lens tube.

14. Reassemble the Z-probe, lens tube, and air assist nozzle.

15. Re-tighten the screws that hold the Z-probe to the lens tube. **Ensure the z-probe holder is tight against the shoulder on the lens assembly. This sets the focal length of the laser.**

16. Wiggle the Z-probe / z-probe bracket to ensure it is **securely fixed** to the lens tube. Re-tighten the screws if required.

16. Re-tighten the thumb-screw that holds the lens tube and Z-probe on the head. **Leave 20mm of spare space as indicated** - this will make it easier to recover from head crashes if required.

17. Check the Z-probe for function. (Push the Z-probe button up; a red light should illuminate on the back of the Z-probe.)

18. Z-datum the machine. **After maintenance there is a increased risk of the Z-probe failing - so really ensure you are ready to E-stop the machine!**

19. Perform another speed test on 3mm MDF and record the result.

