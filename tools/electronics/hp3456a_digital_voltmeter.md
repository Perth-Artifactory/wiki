---
title: HP 3456A 6 1/2 digit voltmeter
description: 
published: true
date: 2022-10-19T10:43:52.798Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:55:44.186Z
---

# HP 3456A 6 1/2 digit voltmeter

\*\* Specifications \*\*

-   Autoranging voltmeter and resistance (2/4 wire)
-   DC Voltage: 100nV to 1000V in 5 ranges
-   DC input impedance \> 10GΩ
-   AC Voltage: 1µV to 700V in 5 ranges
-   Resistance: 1mΩ to 1GΩ
-   Digits 3 1/2, 4 1/2, 5 1/2, or 6 1/2 (depending on integration time (in power line cycles)

NOTE: This device is set up as 60Hz. If you have a spare 4.875MHz crystal, I can set it for 50Hz. Practically speaking, it doesn't make a huge difference)

If you start seeing weird things, the reset button can be used to get back to the initial state. It's far more likely you've turned on a weird function than there is a fault!

This is used basically like a big multimeter. For 2 wire measurements the probes are connected to the Volts/2WΩ/4WΩ connectors; red at the top, black at the bottom. (For 4 wire resistance measurements the additional sense probes are connected to the sense terminals immediately to the left.

The function buttons for DC volts, AC volts, 2 wire resistance, and 4 wire resistance will be the most often used.

By default, 5 1/2 digits are shown. If you want faster readings, this can be reduced to 3 1/2 digits. For 6 1/2 digits resolution the meter must be set to integrate over a longer period.

-   6 1/2 digits:
    -   press "1", "0", "0", "STORE", "CHS"

Note that the CHS button is also labelled "N CYC INT". You have set the integration time to 100 power line cycles, this will enable 6 1/2 digits.

You can set the integration time to .01, .1, 1, 10, or 100 power line cycles. This changes the update speed and the largest number of digits which can be displayed.

Then:

-   6 digit display:
    -   press "6", "STORE", "9"

Note that the "9" button is also labelled "N DIG DISP"

It is also possible to reduce the number of digits displayed by pressing "n", "STORE", "9"; where "n" is 1 thru "6". This allows you to display a smaller number of digits with a longer integration time.

User manual: <http://literature.cdn.keysight.com/litweb/pdf/03456-90006.pdf?id=722597>

This device is typically used as a voltage/resistance meter, but it can do other things including calculations on the measured values, pass/fail measurements, etc. RTFM for more information.

------------------------------------------------------------------------

This meter belongs to Steve Hodges and is on loan to the Artifactory; please do not remove it from the space or try to repair it without first checking with him.
