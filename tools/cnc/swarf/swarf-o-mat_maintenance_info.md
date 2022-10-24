---
title: Swarf-o-mat maintenance information
description: 
published: true
date: 2022-10-19T12:45:24.571Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:54:37.096Z
---

## Swarf-o-mat maintenance information

Swarf-o-Mat (SoM) is a three-axis CNC router originally built by Artifactory member Skot in 2010. It was upgraded in 2020 to its current specification. This page is a technical reference for SoM. For these purposes, SoM is divided into systems for mechanical motion, motion control, power supply, protection, spindle control, cooling and user interface (PC and software).

### Mechanical motion

SoM’s mechanical design fixes the table and achieves x-movement by a moving gantry; y-movement by a carriage on the gantry, and z-movement by moving the spindle on the carriage. All axes use pairs of supported round rods and matching bearings for motion control, and ball screws driven by NEMA23 stepper motors for actuation. The gantry is moved in the x axis by two stepper motors, one driving either end of the gantry. There is no mechanical synchronisation between the two x axis motors, which means that the gantry can become skewed if one motor loses steps or the motors are driven independently. The y and z axes use a single stepper motor each. The stepper motors are NEMA23 form factor, of unknown make and rating. They are 8-wire motors wired for a parallel 4-wire connection.

#### Mechanical alignment procedure

From time to time the machine may need to be aligned to ensure its axes are mutually perpendicular (square to each other). There are three steps to this process:

1\. Make the x-rails co-planar  
Swarfomat's base is relatively flexible in torsion (twisting), which means that the rails are susceptible to losing their correct orientation if the machine base is not level. At the time of writing the base has four feet that simply sit on a table, so rail adjustment is done by putting packers under the appropriate foot. Two methods are suggested for making this correction. In both cases, start by finding two reasonably stiff straight edges (long spirit levels, for example) and placing them across the rails at each end of the machine. Spirit levels are not accurate enough for this operation so ignore the bubble.

The less-accurate, but easier, way is to use a mobile phone inclinometer app to measure the angle of the two straight edges from the horizontal and then pack the feet until the angle is the same to within \~0.1 degree.

The more accurate method is to use a machinist's level and pack the feet to make both straight edges exactly horizontal to within the measurement error of the level.

2\. Square the gantry to the x-rails  
The squareness of the gantry to the x-rails is corrected by moving one or other of the x-axis motors. Since both x rails have their own limit switch, Swarfomat will attempt to self-square whenever the x axis is homed (referenced) by running each motor until its limit switch is tripped, then backing both motors off by an equal amount. Thus the simplest way to make corrections to gantry squareness is to move the limit switch. As a guide, limit switch positions should be accurate to \<0.5mm, which means measurement with a vernier caliper at minimum (a dial gauge also works). The preferred procedure for determining the correction required is:  
2.1 Home the machine on all axes

2.2 Drill four holes in a square in a piece of waste board. This <embed src="/tools/300_sq_8_deep.zip" class="align-center" /> drills holes 8mm deep on a 300mm side and is intended for use with a 6mm drill. Make sure the waste board is thick enough (12mm MDF preferred) and that your starting position will allow the square to be made without hitting the limits.

2.3 Tap a 6mm dowel pin into each hole and accurately measure each diagonal. One method is to hook the end hole of a 300mm steel ruler over one dowel pin and then measure the distance from the flat end of the ruler across the other dowel pin. (I'll eventually make a special tool for this).

2.4 Calculate the required correction as follows:

-   The **angular error** is 2 \* ATAN (AC / BD) - 90 degrees
-   The **linear error** over the square is 300mm \* SIN (angular error) (300mm is the length of a side of the square)
-   The **required correction** is **linear error** \* 650mm / 300mm (650mm is the spacing between the x-rails)

<img src="/tools/swarfomat_gantry_squaring.png" class="align-center" width="600" />

3\. Tram the spindle  
Tramming the spindle means adjusting the spindle so that its axis is perpendicular to the x-y plane. This is done by measuring the distance to the x-y plane from various points on the circle of something being turned in the spindle (the spindle is trammed when the measurement is the same at all points). The preferred method for tramming the spindle is:  
3.1 Establish a reference plane. Place a very flat object on the router table. Most household surfaces are not really flat enough for this purpose, but a piece of glass is OK (a granite or cast iron surface plate is ideal).Place a small packer under three points on the perimeter of the surface so that there are only three points of contact. This will make determining the right adjustments simple. Next, set up a dial indicator to read from the spindle to the reference surface. The dial indicator does not need to be attached to the spindle itself - it can be mounted anywhere on the z-carriage. Move the spindle in x and y to read the distance at the four corners of the reference surface and shim under the packers as necessary to achieve a minimum deviation.

<img src="/tools/swarf_ref_plane_measurement.jpg" class="align-center" width="600" /> Above: one way to measure to the reference plane. Note it is not necessary to mount the indicator in the spindle.

If the rails are parallel it should be possible to get very close to perfect - \<0.02mm or better. If the readings indicate the topology of your 'flat' surface is a saddle, then the rails are not parallel.

By careful placement of the packers and tackling one axis at a time, this procedure can be relatively quick, especially if using feeler gauges as shims (since they have a known thickness).

<img src="/tools/swarf_ref_plane_adjustment.jpg" class="align-center" width="600" /> Above: adjustment of the reference plane.

3.2 Measure the tram of the spindle. Some sort of fitting is required to mount a dial indicator or test indicator on a radius arm attached to the rotating part of the spindle. A test indicator, used flat, may be simpler because height under the gantry is limited and the indicator and arm must be able to rotate through 360 degrees.

<img src="/tools/swarf_tram.jpg" class="align-center" width="600" /> Above: One way to measure tram.

3.3. Correct the spindle in the x-z plane ("nod"). The spindle clamps are mounted to a sub-plate, which is in turn mounted on the z-carriage. x-z adjustment, or nod, is corrected by shimming between the sub-plate and the carriage at either the top or bottom. Thin aluminium about 0.1mm thick is readily available at the Artifactory for this purpose.

<img src="/tools/shim.jpg" class="align-center" width="600" /> Above: The Artifactory has a good supply of shim stock. Shout out to Zen and the Art of Motorcycle Maintenance for the idea.

3.4 Correct the spindle in the y-z plane ("tilt"). The holes in the sub-plate where it is mounted to the z-carriage are oversized allowing a small amount of rotation in the y-z plane. Loosen three of the 4 bolts and adjust as needed. If the required adjustment cannot be got, loosen the fourth bolt.

When you're done you should have tram readings that are identical to within the flatness of the plate plus the put-of-parallel of the rails. Shoot for \<0.05mm, preferably \< 0.02.

### Control Box

The control box contains the controller, breakout board, four stepper motor drivers, 24v and 5v power supplies, a safety relay, DC fuses and hookup wiring.

<img src="/tools/control_box_picture.png" class="align-center" width="1200" />

The control box is connected to:

-   The computer, via an Ethernet crossover cable
-   The stepper motors, via hard-wired connection using one XLR chassis plug per motor:

| Plug | Wire | Colour | Connection at control box | Connection at motor |
|:-----|:-----|--------|:--------------------------|---------------------|
| XLR  | 1    | Blue   | Driver Phase A +          | Phase A +           |
| XLR  | 2    | Red    | Driver Phase A -          | Phase A -           |
| XLR  | 3    | None   | Unused                    | Unused              |
| XLR  | 4    | White  | Driver Phase B +          | Phase B +           |
| XLR  | 5    | Black  | Driver Phase B -          | Phase B -           |

-   The machine limit switches and emergency stop, via hard-wired connections using two RJ-45 chassis plugs (labelled ‘A’ and ‘B’). There is a corresponding terminal box on the machine with RJ-45 plugs broken out to screw terminals for wiring connection. Wire usage is as follows:

| Plug | Wire | Colour        | Connection at control box       | Connection at machine       | Connection at power supply |
|:-----|:-----|---------------|:--------------------------------|:----------------------------|----------------------------|
| A    | 1    | Blue          |                                 | +24v to E stop              | +24v safety relay          |
| A    | 2    | Blue stripe   | CN2 I10+ and relay safety input | E stop contactor 1          |                            |
|      |      |               | CN2 I10-                        |                             | 0v main PSU                |
| A    | 3    | Brown         |                                 | Unused (reserved for probe) | +24v main PSU              |
| A    | 4    | Brown stripe  | CN2 I9+                         | Unused (reserved for probe) |                            |
|      |      |               | CN2 I9-                         |                             |                            |
| A    | 5    | Orange        |                                 | +24v to X limit switches    | +24v main PSU              |
| A    | 6    | Orange stripe | CN2 I8+                         | +X limit switch             |                            |
|      |      |               | CN2 I8-                         |                             | 0v main PSU                |
| A    | 7    | Green stripe  | CN2 I7+                         | -X limit switch             |                            |
|      |      |               | CN2 I7-                         |                             | 0v main PSU                |
| A    | 8    | Green         | CN2 I6+                         | +X2 limit switch            |                            |
|      |      |               | CN2 I6-                         |                             | 0v main PSU                |
| B    | 1    | Blue          |                                 | Unused                      |                            |
| B    | 2    | Blue stripe   | CN2 I5+                         | -X2 limit switch            |                            |
|      |      |               | CN2 I5-                         |                             | 0v main PSU                |
| B    | 3    | Brown         |                                 | +24v to Y/Z limit switches  | +24v main PSU              |
| B    | 4    | Brown stripe  | CN2 I4+                         | +Y limit switch             |                            |
|      |      |               | CN2 I4-                         |                             | 0v main PSU                |
| B    | 5    | Orange        | CN2 I3+                         | -Y limit switch             |                            |
|      |      |               | CN2 I3-                         |                             | 0v main PSU                |
| B    | 6    | Orange stripe | CN2 I2+                         | +Z limit switch             |                            |
|      |      |               | CN2 I2-                         |                             | 0v main PSU                |
| B    | 7    | Green stripe  | Unused                          | Unused                      |                            |
| B    | 8    | Green         | Unused                          | Unused                      |                            |

-   The spindle variable-frequency drive (VFD), via a hard-wired connection using a DIN chassis plug. Wire usage is as follows:

| Plug | Wire | Colour | Connection at control box                                               | Connection at VFD    |
|:-----|:-----|--------|:------------------------------------------------------------------------|----------------------|
| DIN  | 1    | Red    | Controller analog port Pin 6 (Analog Output 1)                          | VI (Voltage Input)   |
| DIN  | 2    | Blue   | Controller analog port Pin 5 (Ground)                                   | ACM (Analog Common)  |
| DIN  | 3    | White  | Breakout board CH1 Output 9 (corresponds to controller Port 2 Output 9) | FOR (Multi-input 1)  |
| DIN  | 4    | Black  | Controller Signal ground                                                | DCM (Digital Common) |

#### Controller and Breakout Board

Intrepretation of G-code commands (e.g. movement instructions) handling of signal inputs (e.g. limit switches and emergency stop) are done by the controller and breakout board. The controller handles all logic while the breakout board provides optical isolation of digital inputs and outputs for protection of the controller. The controller is a <embed src="/tools/uc300eth_manual.pdf" class="align-center" /> and the breakout board is a <embed src="/tools/ucbb_manual.pdf" class="align-center" /> dual-port breakout board.

Stepper motor outputs, limit switch and e-stop inputs, and the 'run' signal for the spindle are wired through the breakout board. Note that the UCBB inputs are extremely flexible and will handle basic mechanical switches, NPN and PNP proximity switches and differential inputs, depending on how they are wired (read the instructions!) The analog speed signal for the spindle is wired directly to the controller.

#### Drivers

Each stepper motor is driven by a digital stepper motor driver that interprets step and direction signals from the controller to energise and de-energise the phases of the connected motor. Each driver allows configuration of maximum driving current and steps per revolution via DIP switches to match the capabilities of the connected motor. The drivers are independently powered, with only signal wiring to the controller The X, X2 and Y drivers are OMC-stepperonline <embed src="/tools/dm556t.pdf" class="align-center" /> drivers, with a maximum current rating of 5.6A. DIP switch settings for these drivers are: 00100011:

001---- 3.2A max  
---0---- Half current when motor is off  
----0011 1600 pulse/rev (8x microstepping)  

The z driver is an omc-stepperonline <embed src="/tools/dm332t.pdf" class="align-center" />, with a maximum current rating of 3.2A. DIP switch settings for this driver are 000101:

000--- 3.2A max  
---101 1600 pulse/rev (8x microstepping)  

#### Power Supplies

There are two power supplies: a 400W 24V supply that powers the stepper motor drivers, the breakout board and the fan; and a 5V 50W supply that powers the controller. Both DC grounds and protective earth are connected to the case.

The 24V supply has three outputs. Two are routed to the stepper motor drivers via the safety relay, and the third bypasses the relay and is connected to the breakout board and fan.

All DC outputs are fused on the positive side. The driver outputs have 10A fuses; the other outputs 5A.

#### Safety Relay

Driver power is routed through a SICK UE48-20S2D2 <embed src="/tools/operating_instructions_ue48_2os_de_en_fr_im0011050.pdf" class="align-center" />. The relay can switch two loads in response to up to two independent enabling inputs. SoM uses only a single input, the e-stop, which requires the inputs to be jumpered together. The relay supports either manual or automatic re-arming after a safety trigger (for SoM automatic re-arming is used, meaning power is restored to the drivers immediately the e-stop is returned to its ready position). The wiring for the relay is as follows:

| Connector | Connection              | Note                              |
|:----------|-------------------------|-----------------------------------|
| A1        | +24V from power supply  | Relay power                       |
| A2        | 0V from power supply    | Relay ground                      |
| 13        | +24V from power supply  | Protected load 1                  |
| 14        | Driver power – X2 and Y | Protected load 1                  |
| 23        | +24V from power supply  | Protected load 2                  |
| 24        | Driver power – X and Z  | Protected load 2                  |
| 31        | Not used                |                                   |
| 32        | Not used                |                                   |
| S11       | RJ45 Plug B Wire 7      | +24V to E-stop contactor 2        |
| S12       | RJ45 Plug B Wire 8, S31 | Enabling input 1, jumpered to S31 |
| S31       | RJ45 Plug B Wire 8, S12 | Enabling input 1, jumpered to S12 |
| S21       | Jumper to S22           | Configures for single input       |
| S22       | Jumper to S21           | Configures for single input       |
| S33       | Jumper to S35           | Configures automatic reset        |
| S34       | Not used                |                                   |
| S35       | Jumper to S33           | Configures automatic reset        |

### Limit switches

The controller has limit switch inputs from both limits of all axes of the machine (pinout as per Table 2), except the -z (lower z) limit. The limit switches are mechanical and are wired normally-closed, each with its own independent controller input. Each side of the x gantry has its own +x and -x limits. The +x, +y and +z limit switches also serve as homing switches.

### Emergency Stop

SoM has an emergency stop (e-stop) prominently mounted on the machine. The functionality on triggering the e-stop is to disable power to the drivers (via the safety relay) and signal an emergency stop to the controller.

### Spindle

Swarfomat uses a 1.5kW water-cooled spindle controlled by a Huanyang HY01D523B<embed src="/tools/huanyang_vfd.pdf" class="align-center" /> (VFD) with a maximum speed of 23040RPM at a driving frequency of 400Hz. The VFD receives an analogue speed signal directly from the controller and a digital enable / disable signal via the breakout board. The spindle has an ER11 collet chuck and can hold tools with a maximum shank diameter of 7mm.

### Cooling

The spindle is cooled by a xxxxxx chiller. The chiller must be running whenever the spindle is running.  
A future project will provide an enable signal from the chiller to prevent the spindle from being started when the chiller is off.
