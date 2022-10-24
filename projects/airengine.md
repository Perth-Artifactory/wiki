---
title: Compressed Air Engine
description: 
published: true
date: 2022-10-19T12:35:50.648Z
tags: 
editor: markdown
dateCreated: 2022-10-19T07:46:33.712Z
---

# Compressed Air Engine

Based on a comment from a visitor to the space, compressed air is freely available at petrol stations (until it is no longer freely available) and can be used to drive an engine mechanism for other purposes.

### Warnings

-   :!: **Compressed air is dangerous** Its ability to turn dust, sand and blockages into projectiles able to pierce skin and eyes should not be ignored.
-   :!: PVC that ruptures under pressure can throw shards like a grenade. It's better not to use PVC, or have an over-pressure release mechanism.
-   Initial prototyping will use a reduced pressure on the outtake rather than high pressure at the intake to create the pressure differential. This will also tend to cause implosion rather than explosion under failure.

## Designs

There are several designs under consideration:

-   based on a two stroke engine, with a single power stroke
-   similar design based on a traditional steam engine, again with a single stroke
-   Flat circular design based on a single large central cog driven by one or more smaller cogs which in turn get driven by a pressure differential.

### 2 Stroke Design

### Steam Engine Design

### Rotary Design

<img src="/projects/airengine_circle.jpg" class="align-center" width="100" alt="airengine_circle.jpg" /> Based on this design which uses smaller cogs on the radius and a fluid pressure on these outer cogs to induce rotation which is in turn transferred to the inner drive wheel. I like this design as it is able to be cut from a single sheet which aids prototyping. It would also look nice with a clear perspex cover (probably reinforced)

#### Phase 1

Design only. Looks like this:

<img src="/projects/airengine1.png" width="100" alt="Air Engine 1" /> ![DXF](/projects/assembly01.dxf.zip)

#### Phase 2

Design and prototype. This extends the design to include 4 small cogs like this:

<img src="/projects/airengine2.png" width="100" alt="Air Engine 2" /> ![DXF](/projects/assemblyx4.dxf.zip)

<img src="/projects/2014-02-01_13.55.42.jpg" width="100" alt="Air2 Prototype" />

The problem with this design is that all cogs are in phase, similar to having a 4-stroke engine where all cylinders are firing at the same time. The prototype also raised an issue where the contact between the cogs was inefficient at a certain point in the cycle. See below the yellow line approximates the line of contact, the red line displays the force transferred to the drive cog, while the blue line shows the preferred line of force. In the prototype the design tended to stick at this point.

<img src="/projects/air2force.png" width="200" alt="Air Engine 2 Forces" />

The proposed solution is in two parts:

-   offset the small cogs to two phases by keeping their position on the circumference but having the inner cog with 2xn cogs rather than 4xn cogs so that two cogs are offset by 90degrees.
-   Look at having small cogs with 6 teeth rather than four

Relating back to the reference design, the inner cog should disconnect early from the outer wall then reconnect late on the small cog in the high pressure area, then disconnect late and reconnect early on the low pressure side.

#### Phase 3

No air holes, but this design keeps the 4 teeth small cogs but offsets the phase of each by 90 degrees so that opposite cogs are synchonised but all four are not.

<img src="/projects/air2.png" width="200" />
