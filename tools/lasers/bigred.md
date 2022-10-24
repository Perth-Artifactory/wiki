---
title: Big Red
description: 
published: true
date: 2022-10-19T12:47:10.401Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:56:59.372Z
---

# Big Red

[Tool Register](/tools/start) - List of all tools

[Laser Cutters General Info](/tools/lasercutters/start) - Info on all laser cutters.

<img src="/tools/lasercutters/big_red_photo.jpg" width="400" />

## Introduction

Our largest and most powerful laser cutter. It's good for large pieces of material, thick material and for cutting quickly. It's suitable for use on wood and acrylic like the other laser cutters. It's not as good at engraving as middle red while little red is better at fine detail work.

Key Parameters:

-   Laser cutter model number: LC1290 (<http://www.wklaser.com/pro_190.aspx>)
-   Controller model number: [MPC6515](/tools/lasercutters/controller_mpc6515)
-   Nominal cut area: 1200mm×900mm
-   Honeycomb area is 1165×862
-   Laser type: CO2 10.6um laser
-   Current laser tube: SPT-TR130 (130W)
-   Laser tube working current: 25-30mA
-   Lens: China PVD Znse Lens 20mm / 63.5 (2.5 inch) ([cloudray](https://www.cloudraylaser.com/products/china-pvd-znse-focusing-lens-for-co2-laser?variant=43422450184))

Computer:

-   Dell 03nvj6 (service tag 1nz282s)
-   Intel Core 2 Duo e7500
-   DDR3 4gb (2x2)
-   AMD Radeon R7 250

## Instructions for Operator

This is the checklist operators should be working through as they go about their laser cutting jobs.

*Click to view larger version (click again for full resolution).*

<img src="/tools/lasercutters/big_red.png" width="300" />

## Laser Tube History

-   2021-now [SPT-TR130](https://www.sptlaser.net/co2-laser-tube/tr-series) (purchased: [aliexpress](https://www.aliexpress.com/item/33026988722.html))
-   2018--2021 100W CO2 laser tube (donated along with Middle Red)
-   2017?--2018 [Reci](http://www.recilaser.com/en/productInfo/fc9181e93b448cac013b44f8a3e20e65.htm) 130W W6 CO2 laser tube, max 26mA)

## General Notes

Big red can cut thicker materials due to a longer focal lens than little red. Big red cannot operate the laser tube at low enough power levels to perform very fine engraving. The step size of big red is larger than the other laser cutters as well which means less fine detail in cuts.

To ensure tube longevity and reliability the tube should **not** be operated above its max working current. This is set by adjusting "laser power percentage" in lasercut software and checking current draw during cutting.

Manual "test" laser fires are currently configured to 10mA, \~40% of the configured Max-Power.

Big Red's cut and engrave speeds are limited to 200mm/s to reduce shaking the mirrors or delicate components out of alignment. Middle red can engrave much faster.

To install the rotary axis for doing round things you need to first disconnect the Y axis and connect the rotary axis.

Note: This page used to be over at [](/lasercutters/lc1290_parameters) but was overhauled and moved here. That page title was: "LC1290 Laser Cutting / Engraving Reference"

Machine Settings:

| X Axis Pulse Unit | 0.0048000000 |
|-------------------|--------------|
| Y Axis Pulse Unit | 0.0048000000 |

The controller is MPC6515: <embed src="/tools/lasercutters/laser_cutter_manual_bigred_mpc6515_20140701113449_50485.pdf" class="align-center" />

The power supply (including screen) is HY-Z from cloudray: <embed src="/tools/lasercutters/hy-z_series_laser_power_supply_user_manual.pdf" class="align-center" />

## Laser Speeds

Cut, engraves and marking speeds are listed here for historical record. Some common and more up-to-date cut speeds will be on the whiteboard next to the laser cutters for common materials. Operators are encouraged to post their cut speeds to \`#lasers-big-red\` on Slack.

### Cutting

Please note that these parameters may not be completely accurate, as they assume that the laser is clean, calibrated and aligned. Always test a small cut on your material before committing to a large job (or be prepared to repeat the cut without moving material).

| Material                          | Thickness | Feedrate  | Power              | Preview Result/notes                                                                                                                                                                                                           |
|-----------------------------------|-----------|-----------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ply                               | 3mm       | 40mm/s    | 100%               | Warps just by looking at it. May benefit from \*careful\* weighting down... \*avoid path of laser head!!\*                                                                                                                     |
| :::                               | 6mm       | 20mm/s    | 100%               |                                                                                                                                                                                                                                |
| :::                               | 9mm       | 10mm/s    | 100%               |                                                                                                                                                                                                                                |
| :::                               | 12mm      | 6mm/s     | 100%               |                                                                                                                                                                                                                                |
| Exterior/Marine Ply               | 4mm       | 17-20mm/s | 100%               |                                                                                                                                                                                                                                |
| :::                               | 6mm       | 5mm/s     | 100%               |                                                                                                                                                                                                                                |
| MDF                               | 3mm       | 35 mm/s   | 100%               |                                                                                                                                                                                                                                |
| :::                               | 6mm       | 20mm/s    | 100%               |                                                                                                                                                                                                                                |
| :::                               | 9mm       | 7mm/s     | 100%               |                                                                                                                                                                                                                                |
| :::                               | 12mm      | 5mm/s     | 100%               |                                                                                                                                                                                                                                |
| Acrylic                           | 3mm       | 25mm/s    | 100%               |                                                                                                                                                                                                                                |
| :::                               | 6mm       |           |                    |                                                                                                                                                                                                                                |
| :::                               | 10mm      | 7mm/s     | 100%               |                                                                                                                                                                                                                                |
| :::                               | 12mm      |           |                    |                                                                                                                                                                                                                                |
| LaserMax                          | 1.6mm     | 200mm/s   | 50%                | (still really powerful!)                                                                                                                                                                                                       |
| Corflute                          | 5mm       | \~40mm/s  | 100%               |                                                                                                                                                                                                                                |
| Hard Range EVA Tile (Black)       | 12mm      | 40mm/s    | 100% (50% corners) | The ones that fit together like a jigsaw. Note that the speed is based on having the hard side at the bottom. Speed can be increased if the hard surface is facing up and faster again if there is no hard side (eg yoga mats) |
| Pine                              | 19mm      | 6mm/s     | 100%               |                                                                                                                                                                                                                                |
| :::                               | 12mm      | 7mm/s     | 100%               |                                                                                                                                                                                                                                |
| Corkboard                         | 6mm       | \-        | \-                 | Will not cut completely without severe charring despite very aggressive parameters. Don't bother. Not yet an approved material.                                                                                                |
| PETG (Polyethylene terephthalate) | 0.5mm     | 120mm     | 40% (Corner 35%)   |                                                                                                                                                                                                                                |

### Engraving

| Material              | Scan Gap | Feedrate | Power | Preview Result                                                                                  |
|-----------------------|:---------|----------|-------|-------------------------------------------------------------------------------------------------|
| MDF                   | 0.075mm  | 200mm/s  | 35%   |                                                                                                 |
| MDF (wide)            | 0.05mm   | 350mm/s  | 25%   | Weird resonance and skipping over a wide (450mm) area using above settings. This worked better. |
| MDF (line)            | na       | 100 mm/s | 25%   | For line work, as opposed to raster engraving. Make sure corner power is set to the same level. |
| Coir Doormat (unused) | 0.5mm    | 350mm/s  | 35%   | Grey scale images do not work.                                                                  |

### Low Powered Line Cut

| Material | Thickness | Feedrate | Power | Preview Result |
|----------|:----------|----------|-------|----------------|
| MDF      | 3mm       | 200mm/s  | 25%   |                |

### From old Maintenance page

Big Red Consumables.

Lense: 20mm Dia, 50.8mm Focal Length, Currently ZnSe, Potentially worth changing to GAAS lense instead?

Mirrors: 25mm Dia, 1st and 2nd mirror are Molybdenum, 3rd Mirror is Silicon Gold. Change all to Molybdenum?

Guide to aligning mirrors on Laser.

<http://justaddsharks.co.uk/support/laser-beam-alignment-guide>

See "[file://filer/shared/member work/lemming/laser alignment](file://filer/shared/member work/lemming/laser alignment)" for laser alignment targets.

### Documents

1.  <embed src="/tools/lasercutters/hy-z_series_laser_power_supply_user_manual.pdf" class="align-center" />
