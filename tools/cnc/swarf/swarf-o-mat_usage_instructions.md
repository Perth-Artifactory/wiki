---
title: Swarf-O-Mat Usage Instructions
description: 
published: true
date: 2022-10-19T12:45:30.445Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:54:47.213Z
---

# Swarf-O-Mat Usage Instructions

## IMPORTANT

### Under NO Circumstances Should you use this Machine if you have not been Trained

Repeat:

**Under NO circumstances should you use this machine if you have not been trained** by an official trainer.

The list of trainers can be found on the the [swarfomat](swarfomat) page.

Very important condition of use: **Use Swarf-o-mat with caution!**

This is a FRAGILE and awesome bit of equipment -- **RESPECT IT, BE CAREFUL!**

If you're not 100% certain about what you're doing, DON'T! Get advice and take care.

## Introduction

If you're new to milling have a read and get familiar with what is involved here:

<http://en.wikipedia.org/wiki/Milling_cutter>

<http://en.wikipedia.org/wiki/Milling_machine>

## Draw your project in VCarve

VCarve is the supported software for use with swarf-o-mat. This software is installed on the computers available in the computer room in the space. Artifactory members can make a folder on the network that can be accessed by swarf-o-mat. Detailed instruction are provided on [VCarve Instructions](VCarve Instructions) page.

Once you have a completed G-Code file, you are ready to proceed to setup.

### Very Important Things that can be Damaged and are Hard to Repair

Be particularly careful of some aspects of the machine.

**The "Jarrah Deck" has been arduously and meticulously made perfect to this machine.**

It's hard-wood and very flat and should **NEVER EVER EVER** be cut.

**Always** make sure that there's a waste-layer buffer between your job and the jarrah deck (there's usually heaps of rubbish/waste sheets next to the machine specifically for this purpose).

**Always** know how deep your job is going to cut. **Is your job going to cut in to the deck?** If so, fix it or buffer it!

**The screw-threads of the base plate**

Do **NOT** screw in too tight to the base plate. If any of these holes become threaded they're very difficult to replace. Be firm but careful.

### Set Up Machine

Turn on the machine at the wall plug. The computer controller and Swarfomat itself will turn on together. The dust extractor should be turned on separately before starting the job.

<img src="/projects/swarfomat_jarrahdeck.jpg" class="align-right" width="300" /> **USE THE MACHINE WITH EXTREME CARE**

If you are not sure what you are doing: **DON'T DO IT**.

Get help and advice from one of the friendly swarf-o-mat operators if in doubt.

Don't "force" anything and remember **safety first**.

#### Setup Project

Be very careful of jarrah deck. See above.

It doesn't really matter where you place your job on the deck, so long as it's entirely within the perimeter.

**RESPECT THE MACHINE**

## Instructions for Use

1.  Place buffer material underneath your job, ensure that the whole area where your job is going to be cut is covered. Its easiest to choose a buffer thats the same size as your raw material.
2.  Clamps are located at the front of the machine. Use at least 4, maybe more depending on the job size. They screw into holes in the bed. Spacers are located in the first drawer - use them to keep the back end of the clamp level.
3.  Insert the appropriate drill bit. You should have decided and specified a drill bit when working with V-Carve. Unscrew the cap from the drill (and remove any drill bit and collet that may have been left). Place your drill bit in the appropriately sized collet and place the collet in the drill. Screw the cap back on. Make sure it's tight!
4.  Mach3 should have started on the computer automatically. Load your job. A picture of the cut should appear on the right-hand window.
5.  Use the arrow keys to move the drill head to the zero point of your job. Make sure to avoid the clamps as you move the head about! Once in position, hit the **Zero X** and **Zero Y** buttons on Mach3
6.  The picture of your job should have adjusted itself to the new co-ordinates. The location of the drill bit is indicated by the crosshairs. Manually check, by moving the drill head to the furthest extents of the job (both X and Y) that the cut is entirely contained within your material, and that the head will not run into any of the clamps.
7.  Move the drill head over a piece of material that will not be part of the finished product. Zero X and Zero Y is often a good location.
8.  Put on safety gear - hearing protection and safety goggles.
9.  Turn on extractor.
10. Turn on Drill
11. **Slowly** and **Carefully** lower the drill (using the PageUp and PageDown keys) so that it just touches the cutting surface. When you hear the sound of the drill starting to bite, stop lowering and hit the **Zero Z** button. Then raise the drill head.
12. You are now ready to cut. Take a moment to review your actions and ensure that all safety precautions have been taken. If being supervised, ask if its OK to proceed.
13. Unlock the console (your trainer will show you how)
14. Press Start.

<img src="/projects/swarfomat_ducting.jpg" class="align-right" width="200" />
