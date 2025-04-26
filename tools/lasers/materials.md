---
title: Laser Material Advice
description: What can I put in the laser cutters?
published: true
date: 2025-04-26T12:51:47.316Z
tags: official
editor: markdown
dateCreated: 2023-02-11T10:17:46.852Z
---

If the material you wish to cut/engrave is not listed as safe on this list, do not cut it without approval from a laser trainer first.

## Wood

### MDF

Medium-Density Fibreboard (MDF) typically cuts quite well on the lasers with the exception of material that has absorbed moisture. The easiest source is Bunnings.

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
| Big Red    | 9     | 12            | 16                          |
| Middle Red | 3     | 6             | 9                           |
| Little Red | 3     | 6             | 9                           |

### Plywood

> Marine Plywood, particularly over 3mm thick, does not cut well on the lasers and may present a fire risk.
{.is-warning}

Plywood is made up of multiple layers of offset wood glued together. This has some advantages and disadvantages. The easiest source is Bunnings.

Considerations:
* **Material variations**: Marine grade plywood (and other fire resistant variations) do not cut well on the lasers and should be avoided. If this material is absolutely required you may have some success using the CNC router instead. You could also cut templates out of another material and use a plunge router depending on your required design.
* **Engraving finish**: Plywood will show wood grain when engraved.
* **Cleanup**: Surface discolouration surrounding cuts/engraves are more common when using Middle Red (less air) but can also be present on Big Red during slower cuts and engraves. It can sometimes be cleaned using Isopropyl Alcohol. Alternatively you may have success sanding the surface of the material (if you are not careful you will sand through the first layer of wood. This will drastically reduce the quality of your material finish in a way that is impractical to recover from.). A lot of this surface discolouration can also be offset by covering the material in masking tape or other contact adhesive backed protecting covering before cutting.
* **Painting**: Plywood paints and seals well.
* **Cut edge properties**: The burnt edge of plywood will not take paint well and has a distinctive finish. Light sanding can fix this but the difficulty is directly related to the complexity of the piece. Additionally unless covered in some way (paint/veneer etc) it will always be easily distinguished as plywood.

Thicknesses:
|            | Works | Edge affected | Edge significantly affected |
|------------|-------|---------------|-----------------------------|
| Big Red    | 9     | 12            | >12                          |
| Middle Red | 3     | 7             | >7                         |
| Little Red | 3     | 7             | >7                          |

### Pine

Considerations:
* **Material variations**: Treated framing pine may present a health risk when cutting.
* **Engraving finish**: Pine will show wood grain when engraved.
* **Cleanup**: The top edges of cut pine will be covered in residue but won't be overly charred. The easiest method of cleanup is likely sanding. A lot of this surface discolouration can also be offset by covering the material in masking tape or other contact adhesive backed protecting covering before cutting.
* **Painting**: Plywood paints and seals well.
* **Cut edge properties**: The edges of cut pine will rarely be perpendicular and will be significantly charred.

### Jarrah

Cuts and engraves well but you will have exceedingly poor results if you have to cut a line twice due to the material hardening once cut. Second passes and slow first passes will present a fire risk.

## Plastic

Certain plastics are completely banned from use on the lasers due to their dangerous byproducts. If you cannot 100% identify the plastic you intend to cut consult with a laser trainer/maintainer before cutting.

### Acrylic

> Mirrored acrylic may present a laser safety hazard to the machine operator. Consult a laser trainer before cutting this variant.
{.is-warning}

* **Material variations**: Apart from mirrored acrylic (see above) The primary safety concern with acrylic variants is when they have a UV coating on top. 
* **Engraving finish**: Will clearly show the individual lines of an engrave unless the passes are quite light or very close together. Running an etch around the outside of engraved areas may provide a more visually distinctive line.
* **Cleanup**: Deep engraves will leave a large amount of powder on the surface of the material. This can be removed using an air compressor and water. The top surface of the acrylic will typically be clear but the bottom may have some residue, particularly on thicker material. This can be somewhat negated by leaving the protective film on the bottom of the material.
* **Painting**: If you're painting the entire material then you're probably better off sourcing a piece that's already the colour you want. For stencil work great success can be had by selectively removing the adhesive paper from the top of the material, painting, then removing the rest. This can be achieved in a few ways (The first will give a more robust finish, the second a smoother surface):
  * Engraving the area you'd like to paint, cleaning the engrave, painting, then peeling the rest of the paper off. or
  * Etching the borders of your desired stencil, carefully peeling off the paper from the parts of the material you want to paint, then painting.
* **Cut edge properties**: Very clean.

### Acrylic laminate (Trolase, Lasermark, Gravoply, etc)

> There are many engraving laminates on the market. Read the following section carefully to confirm that your **exact** material is listed by name below. Do not rely solely on the advice of external suppliers and be wary of substitutions.
{.is-warning}

Acrylic laminate is known under a number of brand names e.g. Trotec Trolase, Rowmark Lasermark, Gravoply Laser, etc.

The material has a thin top layer laminated to a thicker base layer. Lightly engraving the top layer allows the base layer colour to show through.

#### Material variations

The material is available in many thicknesses, colours, printed patterns, and finishes.

The following materials are OK to cut:

* Trotec Trolase
* Rowmark Lasermark
* Gravoply Laser

Consult a laser trainer before cutting laminate materials that aren't on this list.

We strongly recommend that you buy this material from the "laser engraving materials" section of a reputable supplier.

Rotary engraving materials based on ABS will release toxic gasses when lasered. **Do not process ABS material in our laser cutters.** (See: [ABS](https://wiki.artifactory.org.au/tools/lasers/materials#abs).)

Phenolic resin materials (brand name "Traffolyte" or "Gravostrat") release toxic gasses when lasered. **Do not process phenolic resin material in our laser cutters.** The dust from cutting or rotary engraving this material is also toxic.

#### Engraving finish:

Acrylic laminate material is specifically intended for high-resolution laser engraving, and will give excellent results.

The sheet material comes with a layer of clear protective plastic film on the top surface, to protect the surface during shipping and handling. **Remove this clear plastic film before lasering the material.** Leaving the protective plastic film on will result in very poor quality engraving.

The best way to engrave this material is to expose the base layer by engraving away the thin top layer, using the least power possible. You will need to do some testing to find the best settings for each variant of this material.

For Big Red, good starting settings are 400 mm/sec, 10% power and 0.05mm scan gap.

For very fine engravings, reduce the engraving speed (e.g. to 200 mm/sec) so the laser has more time to switch the beam on/off as the head moves over the fine engravings.

#### Cleanup

Wipe with isopropyl alcohol to remove dust and sticky residues. 

To remove coloured residue from white base layers (i.e. red staining on red/white laminate), scrub with a toothbrush and plenty of isopropyl alcohol.

#### Painting 

Typically not required.

#### Cut edge properties

Very clean.

For very clean (glass-like) edges, do 2 cutting passes at reduced power.


### Polyethylene (HDPE) ❌

Polyethylene cuts poorly on laser cutters in part because it melts rather than vapourises. It poses a significant fire risk and has a high likelihood of leaving a residue on the laser bed. It can be safely cut on the [CNC router](/tools/cnc/swarf/swarfomat) instead.

Under heavy supervision by an experienced laser maintainer thin sheets of HDPE may be cut by utilising high airflow to prevent the material from rebonding behind the beam. This is primarily applicable to recycled plastic.

### Polycarbonate ❌

Polycarbonate cuts poorly on laser cutters in part because it melts rather than vapourises. It poses a significant fire risk and has a high likelihood of leaving a residue on the laser bed. It can be safely cut on the [CNC router](/tools/cnc/swarf/swarfomat) instead.

### Polystyrene / Polypropylene ❌

Polystyrene and Polypropylene present a significant fire risk and should not be cut on the lasers at any time. Getting good results on the [CNC router](/tools/cnc/swarf/swarfomat) is potentially difficult and users should consider using alternative tools.

### PVC / Vinyl ❌

> The information below has been included for informational purposes only. This material presents a significant health risk and under no circumstances should be cut on the lasers at any time. Vinyl can be safely cut on the Vinyl cutter located in the Design Lab.
{.is-warning}

PVC contains chlorine which is released when cutting on the lasers in the form of chlorine gas. This gas is harmful to laser componentry and people. Material containing chlorine can be recognised by a yellow smoke being released. If you see this gas immediately press the emergency stop on the machine and step away from the laser until the gas has been extracted. If the laser has been in operation for more than 5 seconds **you must evacuate the courtyard and laser area**. Depending on the respiratory health of attendees on the day they may need to seek emergency medical attention. Alert your nearest committee member if one is present in the space.

### ABS ❌

> The information below has been included for informational purposes only. This material presents a significant health risk and under no circumstances should be cut on the lasers at any time.
{.is-warning}

When burnt ABS releases a variety of gases including hydrogen cyanide which is toxic to people. It also presents a significant fire risk. Users should **consider carefully** before putting 3D printed ABS in the [CNC router](/tools/cnc/swarf/swarfomat) as an alternative.

## Fabric

### Natural fibers

Cut fast to prevent fire. Consider drastically lowering corner power.

### Synthetic cloth

Synthetic fabrics are likely to melt rather than burn. This can result in significant cleanup time and the potential for harmful byproducts. Check with a laser trainer first.

## Paper / Cardboard

> Corrugated cardboard presents a significant fire risk and should be supervised by an experienced laser maintainer.
{.is-warning}

Cuts easily but consider whether the cardboard has a non cuttable plastic coating on it. 

## Leather

> Chrome tanned leather in particular presents a significant health risk and should not be cut at any time.
{.is-warning}

> Faux leather such as PU and vegan leather are not covered by this section
{.is-info}

Vegetable tanned leather is OK to process in our laser cutters.

You must be able to prove to us that the leather is vegetable tanned, i.e. by showing us a label on the material or its packaging, a receipt, or the product description on the website you bought it from.

![veg_tanned_leather.png](/tools/lasers/veg_tanned_leather.png)

Chrome tanned leather is not allowed to be processed in our laser cutters at any time, regardless of whether it is trivalent chromium tanned or hexavalent chromium tanned.

Thin leather cuts well but can have a distinct burnt hair smell. Consider warning people to expect the burnt hair smell before cutting leather in the lasers. If lots of people are in the space (who might be affected by the smell), consider doing your leather processing job another time.

## Glass

> Mirrored glass may present a laser safety hazard to the machine operator. Consult a laser trainer before cutting this variant.
{.is-warning}

Can be etched and (sometimes) scored. Plan for failure and bring extra material. If your goal is to etch a design on the surface this can likely be achieved using a combination of a stencil cut on the vinyl cutter and the sandblaster instead.

## EVA Foam

Cuts great, may need to use engraving passes if doing partial cuts on Big Red because getting the power low enough otherwise is difficult.

## Door mats

> Coir presents a fire risk if the laser power is set too high. Heavily supervise the laser when doing your initial material tests
{.is-warning}

[Doormats made of Coir (coconut) fibre](https://www.bunnings.com.au/40-x-60cm-outdoor-coir-mat_p4490455) engrave well on the laser provided you don't engrave deep enough to hit the bottom rubber layer. On Big Red a fill pass of 600mm/s at 30% power will likely work well.

## Metal

The lasers can't cut metal but they can be used to remove some surface finishes. There's no real risk to the underlying metal if you run the cut too slowly.

### Aluminium Composite Panel (ACP)

Engraving the coloured coating off of this material will result in clean edges but a dirty surface. Wipe with a cloth to clean up the engraved surface.

### Painted Steel

Provided that the paint is laser safe engraves well.

### Anodised Aluminium

Engraves well, may need an etch on the outside of engraved areas to ensure a clean line.

### Metal coated in layout dye/fluid

Engraves well.

### Rusty Iron/Steel

Slight success can be had when engraving designs but the lasers are not a suitable tool for bulk rust removal. Consider the sand blaster or angle grinder instead.

## Laserable rubber (for rubber stamps)

Use specifically laserable rubber, preferably "low odour" laserable rubber. [Pulse Laser Systems](https://pulselasersystems.com.au/product/low-odour-rubber-stamp-sheet-with-adhesive/) is one supplier of this product.

Try the following settings:

* Fill engrave
  * Speed: 100mm/sec
  * Power: 30% max, 10% min
  * Scan gap: 0.100 mm
  * Ramp - under advanced settings - 0.75mm. (This gives the stamp image some angled support material.)
* Cut out
  * Speed: 40 mm/sec
  * Power: 100%

Remember that the stamped image is **mirrored left to right** and the **inverse of what is engraved**.


