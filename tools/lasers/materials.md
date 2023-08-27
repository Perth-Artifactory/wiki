---
title: Materials Advice
description: What can I put in the laser cutters?
published: true
date: 2023-02-16T13:19:02.822Z
tags: official
editor: markdown
dateCreated: 2023-02-11T10:17:46.852Z
---

If the material you wish to cut/engrave is not listed as safe on this list do not cut it without approval from a laser trainer first.

## Wood

### MDF

Medium-Density Fibreboard (MDF) typically cuts quite well on the lasers with one notable exception. The easiest source is Bunnings.

Considerations:
* **Material variations**: Melamine coated MDF cuts well on the laser.
* **Moisture content**: MDF is extremely susceptible to moisture in the air and this will drastically reduce cut speeds and structural stability. Smaller pieces of MDF may be dried in the Artifactory's dry oven.
* **Cleanup**: Surface discolouration surrounding cuts/engraves are more common when using Middle Red (less air) but can also be present on Big Red during slower cuts and engraves. It can sometimes be cleaned using Isopropyl Alcohol. Alternatively you may have success sanding the surface of the material (this may negatively impact the surface of the MDF unless relatively significant effort is put into sanding). A lot of this surface discolouration can also be offset by covering the material in masking tape or other contact adhesive backed protecting covering before cutting.
  * Melamine coated MDF should be cleaned with Isopropyl Alcohol rather than being sanded.
* **Painting**: The same properties that affect MDF's sensitivity to moisture also affect the material when painting. It's common to need more paint than other materials. This can be offset by sealing your pieces after cutting.
* **Cut edge properties**: The burnt edge of MDF will not take paint well and has a distinctive finish. Light sanding can fix this but the difficulty is directly related to the complexity of the piece.

Thicknesses:
|            | Works | Edge affected | Edge significantly affected |
|------------|-------|---------------|-----------------------------|
| Big Red    | 12    | 12            | 16                          |
| Middle Red | 3     | 6             | 9                           |
| Little Red | 3     | 6             | 9                           |

### Plywood

Plywood is made up of multiple layers of offset wood glued together. This has some advantages and disadvantages. The easiest source is Bunnings.

**Marine Plywood**, particularily over 3mm thick, does not cut well on the lasers.

Considerations:
* **Material variations**: Marine grade plywood (and other fire resistant variations) do not cut well on the lasers and should be avoided. If this material is absolutely required you may have some success using the CNC router instead. You could also cut templates out of another material and use a plunge router depending on your required design.
* **Engraving finish**: Plywood will show wood grain when engraved.
* **Cleanup**: Surface discolouration surrounding cuts/engraves are more common when using Middle Red (less air) but can also be present on Big Red during slower cuts and engraves. It can sometimes be cleaned using Isopropyl Alcohol. Alternatively you may have success sanding the surface of the material (if you are not careful you will sand through the first layer of wood. This will drastically reduce the quality of your material finish in a way that is impractical to recover from.). A lot of this surface discolouration can also be offset by covering the material in masking tape or other contact adhesive backed protecting covering before cutting.
* **Painting**: Plywood paints and seals well.
* **Cut edge properties**: The burnt edge of plywood will not take paint well and has a distinctive finish. Light sanding can fix this but the difficulty is directly related to the complexity of the piece. Additionally unless covered in some way (paint/veneer etc) it will always be easily distinguished as plywood.

Thicknesses:
|            | Works | Edge affected | Edge significantly affected |
|------------|-------|---------------|-----------------------------|
| Big Red    | 12    | 18            | 18                          |
| Middle Red | 3     | 7             | \>7                         |
| Little Red | 3     | 7             | >7                          |

### Pine

Cuts and engraves well, more details to come.

### Jarrah

Cuts and engraves well. Can present a moderate fire risk. More details to come.

## Plastic

Certain plastics are completely banned from use on the lasers due to their dangerous byproducts. If you cannot 100% identify the plastic you intend to cut consult with a laser trainer/maintainer before cutting.

### Acrylic

Cuts great, more details to come.

### Polyethylene (HDPE) ❌

Polyethylene cuts poorly on laser cutters in part because it melts rather than vapourises. It poses a significant fire risk and has a high likelyhood of leaving a residue on the laser bed. It can be safely cut on the [CNC router](/tools/cnc/swarf/swarfomat) instead.

Under heavy supervision by an experienced laser maintainer thin sheets of HDPE may be cut by utilising high airflow to prevent the material from rebonding behind the beam. This is primarily applicable to recycled plastic.

### Polycarbonate ❌

Polycarbonate cuts poorly on laser cutters in part because it melts rather than vapourises. It poses a significant fire risk and has a high likelyhood of leaving a residue on the laser bed. It can be safely cut on the [CNC router](/tools/cnc/swarf/swarfomat) instead.

### Polystyrene / Polypropylene ❌

Polystyrene and Polypropylene present a significant fire risk and should not be cut on the lasers at any time. Getting good results on the [CNC router](/tools/cnc/swarf/swarfomat) is potentially difficult and users should consider using alternative tools.

### PVC / Vinyl ❌

> The information below has been included for informational purposes only. This material presents a significant health risk and under no circumstances should be cut on the lasers at any time. Vinyl can be safely cut on the Vinyl cutter located in the Design Lab.
{.is-warning}

PVC contains chlorine which is released when cutting on the lasers in the form of chlorine gas. This gas is harmful to laser componentry and people. Material containing chlorine can be recognised by a yellow smoke being released. If you see this gas immediately press the emergency stop on the machine and step away from the laser until the gas has been extracted. If the laser has been in operation for more than 5 seconds **you must evacuate the courtyard and laser area**. Depending on the respiratory health of attendees on the day they may need to seek emergency medical attention. Alert your nearest committee member if one is present in the space.

### ABS

> The information below has been included for informational purposes only. This material presents a significant health risk and under no circumstances should be cut on the lasers at any time.
{.is-warning}

When burnt ABS releases a variety of gases including hydrogen cyanide which is toxic to people. It also prevents a significant fire risk. Users should **consider carefully** before putting 3D printed ABS in the [CNC router](/tools/cnc/swarf/swarfomat) as an alternative.

## Fabric

### Natural fibers

Cut fast to prevent fire. Consider drastically lowering corner power.

### Synthetic cloth

Synthetic fabrics are likely to melt rather than burn. This can result in significant cleanup time and the potential for harmful byproducts. Check with a laser trainer first.

## Paper / Cardboard

> Corrigated cardboard presents a significant fire risk and should be supervised by an experienced laser maintainer.
{.is-warning}

Cuts easily but consider whether cardboard has a non cuttable plastic coating on it. 

## Leather

Thin leather cuts well but can have a distinct burnt hair smell. Consider cutting outside of events.

> Chrome tanned leather in particular presents a significant health risk and should not be cut at any time.
{.is-warning}

## Glass

Can be etched and (sometimes) scored. Plan for failure and bring extra material. More details to come.

## EVA Foam

Cuts great, may need to use engraving passes if doing partial cuts on Big Red because getting the power low enough otherwise is difficult.