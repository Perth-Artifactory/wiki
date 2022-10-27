---
title: Swarf-O-Mat CNC Router
description: 
published: true
date: 2022-10-20T12:32:28.974Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:54:57.788Z
---

# Swarf-O-Mat CNC Router

## Summary

<img src="/projects/swarfomat_jarrahdeck.jpg" class="align-left" width="300" alt="swarfomat_jarrahdeck.jpg" /> The Swarf-O-Mat is a CNC router that can machine wood, plastics and soft metals. Swarf-O-Mat was built by [skot](/user/skot) in 2010, back before AliExpress was a thing, and donated to the Artifactory. There is a small selection of Artifactory-owned tooling available, but regular users will want to purchase their own tooling (the charge for use is lower if users supply their own tooling).  
  
:!: As with all CNC machines, learning to use Swarf-O-Mat safely (for the user and the machine) requires a significant investment of time. Without appropriate training, the machine has the potential to be **very** dangerous. As such, it is 'gated' and you may not use it until you have been trained.

## Hazards

![movingpng.png](/resources/hazards/movingpng.png)

## Approved Users

Under NO circumstances should you use this machine if you have not been trained. ... \|\< 100% 20% \>\| \^ Trainers \^ Availability \^ Availability

| Trainers                                 | Availability                             |
|------------------------------------------|------------------------------------------|
| [Jason Kongchouy](/user/Jason Kongchouy) | General Hacking Days, by request (Slack) |
| Fletcher Boyd                            | General Hacking Days, by request (Slack) |
| Iain Graham                              | Open days, by request (Slack)            |
| Ben Connor                               | By request (Slack)                       |

| Full Operators         |
|------------------------|
| [maxlex](/user/maxlex) |
| Glenn Martin           |
| [timbo](/user/timbo)   |
| [elena](/user/elena)   |
| Jenna Downing          |
| Mike                   |
| Nathan Thompson        |
| Joshua                 |
| Vincent Dalstra        |
| Nick Bannon            |
| Beau Daley             |
| Ben Connor             |
| Glynn                  |
| O Nokey                |
| Tom White              |

## Tool Usage Fee

Refer to [Tool Usage Fees](/docs/policies/fees).


## Swarf-o-Mat Reference

| Materials Reference |             |                      |                 |                                                             |
|---------------------|-------------|----------------------|-----------------|-------------------------------------------------------------|
| Material            | VFD Setting | Feed Rate (6mm Tool) | Pass Depth (mm) | Notes                                                       |
| Aluminium           | 400         | 200mm/min            | 0.25            | Swarf will re-weld to sides of channels - keep job clean    |
| HDPE                | 300         | 1200mm/min           | 3               | Cuts like butter                                            |
| Perspex / Acrylic   | 300         | 600mm/min            | 2               | Grind the plastic, don't melt it - take it slower than wood |
| Jarrah              | 400         | 800mm/min            | 2               | Jarrah gets even HARDER if burnt                            |
| Pine                | 400         | 1300mm/min           | 3               | Forgiving & easy                                            |
| MDF                 | 400         | 1300mm/min           | 3               | Easy to cut, but dust is toxic                              |

## Specifications

| X Axis Range                  | 600                                 |
|:------------------------------|-------------------------------------|
| Y Axis Range                  | 420                                 |
| Z Axis Range                  | 70                                  |
| Collet                        | ER11                                |
| Driver Software               | Mach3                               |
| Full Swarf-O-Mat Area         | 600mm x 460mm x 70mm (minus buffer) |
| Maximum Dimensions of Any job | **580mm x 440mm x 60mm**            |

## Approved Materials

You can **not** use a lot of things, if it's not listed here and/or you're not sure ASK!

|                |
|----------------|
| \< 100% 20% \> |
| Material       |
| soft wood      |
| MDF            |
| acrylic        |
| HDPE           |
| hard wood      |
| aluminium      |

## Swarf-O-Mat Checklist

-   Computer, controller and chiller powered on
-   Check table is clear and no mechanical obstructions to movement
-   Reference (home) all axes. X axis should self-square when referenced
-   Switch on soft limits (not compulsory, but recommended)
-   Clamp job tightly with spoil board underneath
-   Check clamps and biscuits clear of moving gantry
-   Install collet into collet nut. IMPORTANT- this must be done before the tool is installed in the collet.
-   Install cutting tool in correct-sized collet and tighten with spanners
-   Load g-code and check the tool path appears correct
-   Move to desired zero locations and x and y axes
-   Optional: zero z axis with clearance above the workpiece and do a dry run 'cutting air'
-   Move to the desired zero location and zero the z axis
-   Move clear of the workpiece
-   Check cooling water is flowing
-   Turn on room fan and dust extractor
-   Turn on PPE light
-   Check all present are wearing safety gear. Eye protection is mandatory. Hearing protection is recommended.
-   If your G-code does not include spindle control, set the spindle speed and turn the spindle on
-   Begin the job
-   Turn off spindle
-   Remove job and spoilboard
-   Pack away clamps, biscuits and tools
-   Clean up using the vacuum cleaner
-   Log out
-   Power off computer, controller and chiller
-   Report any problems to \#tools_and_fabrication.

## Instructions for Use

<img src="/process_guide/vcarve_letter_t_animated.gif" class="align-right" /> Very important condition of use: **Use Swarf-o-mat with caution!**

This is a FRAGILE and awesome bit of equipment -- **RESPECT IT, BE CAREFUL!**

If you're not 100% certain about what you're doing, DON'T! Get advice and take care.

#### 1) Know what you want to make/do

If you're here, hopefully you already have plans.

**You can:**

-   cut
-   engrave
-   carve (to a limited extent)

=== 2) Plan and draw your project in VCarve ===

VCarve is the supported software for use with swarf-o-mat.

This software is installed on the computers available in the computer room in the space.

Artifactory members can make a folder on the network that can be accessed by swarf-o-mat.

Detailed instruction are provided on [VCarve Instructions](VCarve Instructions) page.

#### 3) Cut material with swarf-o-mat

**USE THE MACHINE WITH EXTREME CARE**

If you are not sure what you are doing: **DON'T DO IT** -- get help and advice from one of the friendly swarf-o-mat operators.

Detailed instruction are provided on [Swarf-O-Mat Usage Instructions](Swarf-O-Mat Usage Instructions) page.

## Quick and dirty notes on spindle speed control

As of 20/6/21 Swarf-o-mat is configured for software control of spindle speed (including start/stop). Spindle speed can be set in three ways:

#### Spindle control through Mach3 UI

The spindle speed can be set through the Mach3 UI, in the lower right corner of the main (Program Run) screen: <img src="/tools/speed_control_picture.png" class="align-center" width="400" />

#### Spindle control in g-code

The spindle can be started or stopped, or speed controlled, with g-code commands, either entered through the Mach3 UI on the MDI page or embedded in your program:

-   M3 starts the spindle
-   M5 stops the spindle
-   Sx sets the speed to x RPM

Once set, the spindle speed can be overridden through the Mach 3 UI

#### Spindle control through VFD touch pad

Should you want to return Swarfomat to spindle control through the touchpad, please change **only the VFD settings**. Do not mess with the Mach 3 setup. The relevant VFD settings are:

-   PD001, which determines the source of run commands. 0 denotes control from the touchpad, 1 denotes control via digital input.
-   PD002, which determines the source of speed commands. 0 denotes control from the touchpad, 1 denotes control via 0-10v analog input.

Instructions on how to change the settings through the touchpad are in the <embed src="/tools/huanyang_vfd.pdf" class="align-center" />.

## Documentation

| Document                                                                                           | Notes                                               |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <embed src="/tools/huanyang_vfd.pdf" class="align-center" />                                       | Reference for the Huanyang variable-frequency drive |
| <embed src="/tools/uc300eth_manual.pdf" class="align-center" />                                    | Reference for the CNCDrive UC300ETH controller      |
| <embed src="/tools/ucbb_manual.pdf" class="align-center" />                                        | Reference for the UCBB breakout board               |
| <embed src="/tools/dm332t.pdf" class="align-center" />                                             | Reference for the z-axis driver                     |
| <embed src="/tools/dm556t.pdf" class="align-center" />                                             | Reference for the x- and y-axis drivers             |
| <embed src="/tools/operating_instructions_ue48_2os_de_en_fr_im0011050.pdf" class="align-center" /> | Reference for the safety relay                      |
| <embed src="/tools/mach3mill_1.84.pdf" class="align-center" />                                     | Installation and user guide for Mach3 Mill          |
| Chiller                                                                                            | Instruction manual for the spindle cooler           |

## Notes

Details of Swarfomat's configuration are available on the [maintenance information page](/tools/ swarf-o-mat_maintenance_info).  
Information relating to the original build is available on the original [Project Page](/projects/swarf-o-mat).
