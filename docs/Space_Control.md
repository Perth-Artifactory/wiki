---
title: Space Control
description: Relays and buttons oh my!
published: true
date: 2023-07-11T15:21:10.756Z
tags: official
editor: markdown
dateCreated: 2023-03-01T15:54:50.097Z
---

Some of the devices around the workshop have migrated to an electronic control system. While a manual override is possible the intention is that attendees utilise Artifactory workstations, the foyer kiosk, or their personal devices to control things. In many cases the devices are automated and don't need to be interacted with.

You can access the [control panel](https://control.artifactory.org.au) when connected to the WiFi or from the kiosk in the foyer. (It's a Home Assistant instance)

## Areas

| What                    | Automations | Manual | Override |
|-------------------------|-------------|--------|----------|
| Project area bay lights | All on by default when the main light switches are used | Home Assistant | Turn the workshop lights off for 5 seconds and then turn them back on. |
| Carpark lights | Turned on for 5 minutes when the kiosk `leaving` button is pressed after sunset or if the timer button is pressed. | Silver button to the left of the front door | None (silver button has no external requirements) |
| Courtyard lights | None | Silver button below roller door controls or via Home Assistant | None (silver button has no external requirements) |
| Mill / Lathe | None | Silver button on the side of the mill wall/shield or via Home Assistant | None (silver button has no external requirements) |
| Machine room | Front and back switches will both toggle the entire room. Switch will turn on automatically when door is opened. | Silver buttons next to the door or behind bandsaw. Alternatively via Home Assistant | None (silver buttons has no external requirements) |
| Social area light | Turns on with scheduled event | White button on social table next to phone charger | None, hardwired |
| Workshop lights | Turns on after a key is scanned on the front door | Light switch on side of switchboard inside front door | None (light switch has no external requirements) |

## Decorations

| What                    | Automations | Manual | Override |
|-------------------------|-------------|--------|----------|
| Bar                     | **Turns on** when a Google calendar event starts<br>**Turns off** when the event ends | Home Assistant | Button on the relay behind the left side of the bar |
| Foyer                   | **Turns on** when a Google calendar event starts<br>**Turns off** when the event ends | Home Assistant | Button on the relay on the top of the wall (near the GPO) |
| Robot (Electronics Lab) | **Turns on** when a Google calendar event starts<br>**Turns off** when the event ends | Home Assistant | Button on the relay inside the body |
| Battlestar Galactica    | Turns on with the bar | | |
| Blimp                   | **Turns on** when a Google calendar event starts | Home Assistant | None, Hardwired |
| Pallet rack lighting | **Turns on** when a Google calendar event starts | Home Assistant | Paddle switch above the power board tub |

## Aircon

| What                    | Automations | Manual | Override |
|-------------------------|-------------|--------|----------|
| Electronics Lab | N/A | Button on front of aircon | N/A |
| Rehearsal Room  | **Turns on** 30 minutes before a room booking<br>**Turns off** 30 minutes after a room booking or after the aircon has been on for 4 hours (whichever comes first) | Button on front of TP-Link switch outside design lab | Plug directly into GPO |
| Design Lab      | N/A | Button on wall next to resin printers | N/A |
