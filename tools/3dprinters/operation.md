---
title: 3D Printer Operation Checklist
description: 
published: true
date: 2024-07-22T05:58:28.874Z
tags: 
editor: markdown
dateCreated: 2024-04-26T08:01:22.593Z
---

> This is an in progress draft document.
{.is-info}


> You need to be trained (and pass a test) before using our 3D printers.
>
> Only current, authorized [printer trainers](/tools/3dprinters#trainers) can deliver printer training.
{.is-warning}

You can follow these guides on any of our 3D printers. When steps deviate between printers there will be a section for each printer. An example is included below:

<details>
  <summary>Printer 1</summary>
  Press the red button
</details>
<details>
  <summary>Printer 2</summary>
  Press the Blue button
</details>

## FDM / Filament

* Determine the best configuration for your print in line with the [5 factors](/tools/3dprinters/factors).
* Slice your print
<details>
  <summary>Bambu Labs P1S</summary>
  Using Bambu Studio
</details>
<details>
  <summary>Ender 3 V2 Neo, Prusa Mk4, Prusa XL</summary>
  Using PrusaSlicer
</details>

* Transfer your sliced file to the printer
<details>
  <summary>Bambu Labs P1S</summary>
  
  * Select *Print plate*/*Send*
  * Ensure AMS mapping has been successful
  * Check/uncheck *Bed Levelling* as appropriate
  * Press *Send*
  
</details>
<details>
  <summary>Ender 3 V2 Neo</summary>
  
  * Take the Micro SD card from the front left of the machine and plug it into the card reader attached to the slicing PC
  * Press the *Export to SD card/Flash drive* button within PrusaSlicer and specify a filename
  * Reinsert the Micro SD card in the printer
  
</details>
<details>
  <summary>Prusa Mk4</summary>
  
  * Ensure that the **physical** printer `Artifactory-Mk4-1` is selected
  * Press *Send to printer* in the bottom right
  
</details>
<details>
  <summary>Prusa XL</summary>
  
> Sending files to the XL is possible but is very slow. The process below is recommended.
{.is-info}

  
  * Take the USB Drive from the right hand side of the printer control panel and plug it into the slicing PC
  * Press the *Export to SD card/Flash drive* button within PrusaSlicer and specify a filename
  * Reinsert the USB Drive into the printer.
  
</details>

* Ensure that the printer is set up with the nozzle and bed you selected when setting up your print
* Ensure there's no filament buildup on the nozzle
* Ensure all filament has been removed from the build plate
* Clean the build plate
* Remove the current filament from the printer - Make sure the filament is secured to the spool once it has been removed
<details>
  <summary>Bambu Labs P1S</summary>
  
  * Open the AMS
  * Unload the active filament if required - The active filament is the spool currently loaded into the print head and is indicated by a slowly pulsing white light. You can instruct the printer to unload the spool from the control panel or Bambu Studio.
  * Push the grey tab away from you to back off the feeder and wind the filament back onto the spool
  
</details>
<details>
  <summary>Ender 3 V2 Neo</summary>
  
  >   Be gentle! One of our trainers will show you how much force to use
{.is-info}
  
  * Set the nozzle temperature to 250C
  * Wait for the nozzle to hit 250C
  * De-tension the extruder and remove the filament
  
</details>
<details>
  <summary>Prusa Mk4, Prusa XL</summary>

  * Select *Filament* -> *Change Filament*
  * Follow the on screen instructions
  
</details>

* Load the correct filament into the printer
<details>
  <summary>Bambu Labs P1S</summary>
  
  * Place the filament into the AMS
  * Push the filament into the feeder (aprox 100mm) and release the grey tab 
  * You've completed this step correctly if the AMS pulls the filament deeper into the machine
  
</details>
<details>
  <summary>Ender 3 V2 Neo</summary>
  
>   Be gentle! One of our trainers will show you how much force to use
{.is-info}
  
  * Set the nozzle temperature to 250C
  * Wait for the nozzle to hit 250C
  * De-tension the extruder and push the filament through all the way through the filament path to the nozzle.
  * Keep pushing until the filament coming out of the nozzle is the correct colour.
  
</details>
<details>
  <summary>Prusa Mk4, Prusa XL</summary>

  * If you used *Unload filament* instead of *Change filament* select Filament -> *Change filament*
  * Follow the on screen instructions
  
</details>

* Confirm that there is enough filament on the current spool for your job and take appropriate measures if not
<details>
  <summary>Bambu Labs P1S</summary>
  
  * Load a second spool of the same filament into another slot on the AMS
  * Ensure that both spools are set to identical materials and colours
  * Ensure "AMS filament backup" is enabled. It can be found under the AMS settings on the devices page of Bambu Studio
  
</details>
<details>
  <summary>Ender 3 V2 Neo</summary>
  
  * This printer is not capable of detecting when a spool runs out. If you think this might happen we suggest using a different printer.
  
</details>
<details>
  <summary>Prusa Mk4</summary>

  * While this printer cannot automatically change to a second spool it will pause when it runs out of filament. When this happens simply load a second spool into the machine using the steps outlined above and resume the print.
  
</details>
<details>
  <summary>Prusa XL</summary>

  * Load a roll of the same filament into an unused head
  * After you've pressed print select the second spool and link it to the first material by selecting "Spool Join"
  
</details>

* Remove the lid if printing PLA on the Bambu Labs P1S
* Start the print
* Monitor the first layer for plate adhesion
* Periodically check in on your print while in the workshop
* Wait for your print to complete
* Remove your part from the build plate. This may involve removing the build plate from the printer so it can be lightly flexed:

> Oil from your hands will reduce bed adhesion and is one of the most common things you're cleaning from the bed, consider wearing nitrile gloves for this step.
{.is-info}

<details>
  <summary>Bambu Labs P1S</summary>
  
  * Lift the build plate off the bed by the two tabs at the front
  * Lightly flex the bed to remove your part
  * Reseat the build plate on the printer using the seating guides on the back left and back right corners of the bed
  
</details>
<details>
  <summary>Ender 3 V2 Neo</summary>
  
  * Lift the build plate off the bed using the two tabs at the front
  * Lightly flex the bed to remove your part
  * Reseat the build plate on the printer. There are no assistive pins/markers for this.
  
</details>
<details>
  <summary>Prusa Mk4</summary>

  * Lift the build plate off the bed by two front tabs
  * Lightly flex the bed to remove your part
  * Reseat the build plate by seating the back slot with the two pins on the back of the bed
  
</details>
<details>
  <summary>Prusa XL</summary>

  * Go to *Control* -> *Pick/Park Tool*
  * Lift the build plate off the bed by the two tabs at the front
  * Lightly flex the bed to remove your part
  * Reseat the build plate by seating the back slot with the two pins on the back of the bed
  * Bend the build plate gently and lower back down onto the machine starting from the back
  
</details>

* Ensure the build plate and nozzle are clean for the next print/user
