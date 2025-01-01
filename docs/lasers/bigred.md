---
title: Big Red - Maintenance notes
description: Information on this page is largely only useful for equipment maintainers
published: true
date: 2024-01-04T10:16:43.769Z
tags: 
editor: markdown
dateCreated: 2024-01-04T10:16:43.769Z
---

# Big Red - Maintenance

Details on this page have been moved from the primary [Big Red](/tools/lasers/bigred) page as they're not really applicable to operators.

## Specs

| -------------------------- | ----------------- |
| Make/Model                 | [G.Weike LC1290](https://web.archive.org/web/20150319072633/http://www.wklaser.com/pro_190.aspx) |
| Controller                 | [MPC6515](/tools/lasers/controller_mpc6515) |
| Nominal cut area           | 1,200 × 900 mm    |
| Honeycomb area             | 1,165 × 862 mm    |
| Laser type                 | CO2 10.6μm laser  |
| Laser tube                 | SPT-TR130 (130W)  |
| Laser tube working current | 25 - 30mA         |
| Lens                       | China PVD Znse Lens 20mm / 63.5 (2.5 inch) ([Cloudray](https://www.cloudraylaser.com/products/china-pvd-znse-focusing-lens-for-co2-laser?variant=43422450184)) 

## Computer

-   Dell 03nvj6 (service tag 1nz282s)
-   Intel Core 2 Duo e7500
-   DDR3 4gb (2x2)
-   AMD Radeon R7 250

## Laser Tube History

-   2021-now [SPT-TR130](https://www.sptlaser.net/co2-laser-tube/tr-series) (purchased: [aliexpress](https://www.aliexpress.com/item/33026988722.html))
-   2018--2021 100W CO2 laser tube (donated along with Middle Red)
-   2017?--2018 [Reci](http://www.recilaser.com/en/productInfo/fc9181e93b448cac013b44f8a3e20e65.htm) 130W W6 CO2 laser tube, max 26mA)

## Settings

|-------------------|--------------|
| X Axis Pulse Unit | 0.0048000000 |
| Y Axis Pulse Unit | 0.0048000000 |

We do not have a user manual for the LC1290 specifically. [operational_manual_of_machine_xin_usb.pdf](/tools/lasers/operational_manual_of_machine_xin_usb.pdf) is a manual for the similar (but not identical) LC1280.

The controller is MPC6515: [laser_cutter_manual_bigred_mpc6515_20140701113449_50485.pdf](/tools/lasers/laser_cutter_manual_bigred_mpc6515_20140701113449_50485.pdf)

The power supply (including screen) is HY-Z from Cloudray: [hy-z_series_laser_power_supply_user_manual.pdf](/tools/lasers/hy-z_series_laser_power_supply_user_manual.pdf)

## From old Maintenance page

Big Red Consumables.

Lense: 20mm Dia, 50.8mm Focal Length, Currently ZnSe, Potentially worth changing to GAAS lense instead?

Mirrors: 25mm Dia, 1st and 2nd mirror are Molybdenum, 3rd Mirror is Silicon Gold. Change all to Molybdenum?

Guide to aligning mirrors on Laser.

<http://justaddsharks.co.uk/support/laser-beam-alignment-guide>

See `\\filer\Resources\Laser\laser-Alignment-target\` for laser alignment targets.

### Documents

1.  <embed src="/tools/lasercutters/hy-z_series_laser_power_supply_user_manual.pdf" class="align-center" />