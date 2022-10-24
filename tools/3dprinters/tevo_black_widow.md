---
title: Tevo Black Widow FDM 3D Printer
description: 
published: true
date: 2022-10-19T12:45:07.024Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:54:05.862Z
---

# Tevo Black Widow FDM 3D Printer

## Summary

<img src="/tools/tevo.jpg" width="300" alt="tevo.jpg" /> The Tevo is a filament deposition method (FDM) 3D printer that can print a variety of filaments.  
  
  

## Hazards

|                                   |
|-----------------------------------|
| \< 80% 200px 500px 200px 500px \> |
| ![](/tools/hazards/fire.svg)      |

3D printers are relatively safe as long as they are properly built and maintained. If they are not, they potentially pose both a fire and an electrical hazard. **If anything about the printer's appearance, sound, smell or performance suggests a problem, then turn it off, place an "out of order" sign on it and notify the \#3d-printing Slack channel**  
===== PPE Required ===== None

## Authorised Users

This printer is available for everyone to use. However it is recommended that you seek a brief familiarisation from an experienced user, particularly if you are new to 3D printing. Use the \#3D-printing channel on Slack to find someone who can help.

## Specifications

|                          |
|--------------------------|
| \< 80% \>                |
| Print volume (X x Y x Z) |
| Materials                |
| Controller               |
| Firmware                 |

## Instructions for Use

### Slicing

Any slicing software that produces Marlin-compatible gcode can be used to prepare prints. The design lab computers have Prusa Slicer installed on them with printer profiles for the Tevo. Note there are two profiles: one with start g-code to do a mesh bed levelling before printing, and one without (the profiles are otherwise identical).

### Bed Preparation

The printer has a glass heated bed which needs to be coated with glue stick before printing. One application of glue stick will last several prints, after which the bed should be cleaned and glue stick re-applied. The glass surface can be removed and washed with hot water to clean off the old glue stick.

### Printing

Prints can be made from g-code files on an SD card (the slot is in the left side of the control box).

The machine's menu structure is navigated by turning the dial to highlight a menu item, then pushing it in (audible click) to select. Some useful menu items include:

| Path                                          | Action                                                    |
|-----------------------------------------------|-----------------------------------------------------------|
| Main=\>Print from media                       | Select a file to print                                    |
| Main=\>Motion=\>Auto home                     | Home all axes                                             |
| Main=\>Motion=\>Move axis                     | Move one axis                                             |
| Main=\>Motion=\>Bed leveling=\>Level bed      | Conduct mesh bed levelling                                |
| Main=\>Motion=\>Bed leveling=\>Probe z offset | Make adjustments to z home position relative to the probe |
| Main=\>Motion=\>Bed leveling=\>Store settings | Save bed mesh data and z offset                           |
| Main=\>Temperature=\>Preheat PLA / PETG       | Heat hotend, bed or both in preparation for printing      |
| Main=\>Tune=\>Nozzle (while printing)         | Adjust the hotend temperature while printing              |
| Main=\>Tune=\>Bed (while printing)            | Adjust the bed temperature while printing                 |
| Main=\>Tune=\>Fan (while printing)            | Adjust the fan speed while printing                       |
| Main=\>Tune=\>Babystep Z (while printing)     | Micro-adjust the z-position of the nozzle while printing  |

### z height adjustment

The height of the nozzle relative to the bed is very important for ensuring the first print layer sticks to the bed. Z height should not routinely need to be adjusted provided that Probe z offset is set correctly, mesh bed levelling is used periodically and the bed is not physically moved up or downon the adjusting screws. If z height does need to be re-set, the procedure is:

-   Level the bed as closely as possible on the levelling screws by moving the nozzle to each corner of the bed in succession and using a piece of paper to get the clearance between nozzle and bed approximately equal
-   Perform mesh bed levelling from the menu and save the setting
-   Print a one-layer test square (g-code file here), making babystepping z adjustments until a good first layer is obtained.
-   Enter the amount of babystepping z adjustment into the Prove z Offset and save the settings.

#### Warning

Do not move the bed or carriage by hand while the stepper motors are plugged in. The movement can induce a high voltage that may damage the stepper motor drivers.

## Technical notes

### Controller

The Tevo runs a BigTreeTech SKR 1.3 32-bit control board with DRV8825 drivers for the stepper motors. Uploading firmware to the board is done by copying the firmware.bin file onto a microSD card and insertign the card into the slot on the controller. The firmware is automatically updated when the board is restarted.

The pin configuration of the controller is standard except that the hotend fan is configured to run from the second hotend (HE1) PWM output. This allows the hotend fan to be automatically switched off when the hotend is below 50 deg.

### X-Carriage hardware

The Tevo's x-carriage has:

-   An E3D Titan (or clone) extruder
-   A 24V E3D V6 hotend with 0.4mm brass nozzle
-   A BL Touch z-probe that is used for both homing and mesh bed levelling
-   Hotend and part cooling fans.

The the extruder, BL Touch probe and part cooling fan mounts, and the part cooling fan duct, are custom-designed 3D printed parts (files are <embed src="/tools/printed_parts.zip" class="align-left" />).

### Heated bed

The Tevo has a large and power-hungry heated bed that, on early models, burned out their controllers' MOSFETs. This one has an add-on external MOSFET that runs the heated bed and is powered directly from the power supply.

### Firmware

The Tevo runs Marlin 2.0.7.2. The Marlin source files are <embed src="/tools/marlin-2.0.x.zip" class="align-left" />, and a copy is also on the MicroSD card installed in the controller. Other than the standard configuration items for any printer, notable firmware configuration features are:

-   Addition of \_Bootscreen.h to provide the custom Artifactory bootscreen
-   Restriction of maximum accelerations, reflecting that teh macine is heavy in all axes
-   Inclusion of the BL Touch
-   Inclusion of auto bed levelling
-   Inclusion of the ability to persist settings in the EEPROM
-   Setting the second preheat filament type to PETG (since it is more likely to be used than ABS)
-   Scaling the part cooling fan output down by 50% (at 100%, excessive cooling prevents adjacent layers from sticking)
-   Setting the HE1 pin to drive the hotend cooling fan
-   Inclusion of babystepping for all axes

## Documentation

Ha. The factory manual for this machine is hilarious, but not much use. There is however a <embed src="tevo-black-widow_1_.pdf" class="align-left" />, which has a lot of generally useful / interesting information, albeit chaotically presented.

If you use, or want to use, PrusaSlicer to prepare your models for printing, there are good online instructions [here](https://help.prusa3d.com/en/category/prusaslicer_204).
