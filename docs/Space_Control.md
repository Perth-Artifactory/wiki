---
title: Space Control
description: Relays and buttons oh my!
published: true
date: 2023-03-01T15:54:50.097Z
tags: official
editor: markdown
dateCreated: 2023-03-01T15:54:50.097Z
---

# How to control the space

Some of the devices around the workshop have migrated to an electronic control system. While a manual override is possible the intention is that attendees utilise Artifactory workstations, the foyer kiosk, or their personal devices to control things. In many cases the devices are automated and don't need to be interacted with.

You can access the [control panel](https://control.artifactory.org.au) when connected to the wifi. (It's a Home Assistant instance)

## Lights

| What                    | Automations | Manual | Override |
|-------------------------|-------------|--------|----------|
| Project area bay lights | N/A | Home Assistant | Turn the workshop lights off for 5 seconds and then turn them back on. |

## Decorations

| What                    | Automations | Manual | Override |
|-------------------------|-------------|--------|----------|
| Bar                     | **Turns on** when a google calendar event starts<br>**Turns off** when the event ends | Home Assistant | Button on the relay behind the left side of the bar |
| Foyer                   | **Turns on** when a google calendar event starts<br>**Turns off** when the event ends | Home Assistant | Button on the relay on the top of the wall (near the GPO) |
| Robot (Electronics Lab) | **Turns on** when a google calendar event starts<br>**Turns off** when the event ends | Home Assistant | Button on the relay inside the body |
| Battlestar Galactica    | Turns on with the bar |||
| Blimp                   | N/A | Bottom left switch on the laser GPOs | N/A |

## Aircon

| What                    | Automations | Manual | Override |
|-------------------------|-------------|--------|----------|
| Electronics Lab | N/A | Button on front of aircon | N/A |
| Rehearsal Room  | **Turns on** 30 minutes before a room booking<br>**Turns off** 30 minutes after a room booking or after the aircon has been on for 4 hours (whichever comes first) | Button on front of TP-Link switch outside design lab | Plug directly into GPO |
| Design Lab      | N/A | Button on wall next to resin printers | N/A |