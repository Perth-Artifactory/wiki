---
title: Training formatting guide
description: 
published: true
date: 2025-09-05T08:04:32.404Z
tags: restricted-officer
editor: markdown
dateCreated: 2025-09-04T23:28:05.368Z
---

Resources in this section are intended to:

* Set a minimum standard of information provided in inductions
* Act as a checklist for trainers during an induction
  * Resources are primarily consumed by trainers from their phones while standing at a machine
  * If adding supporting material, include it at the end
* Be read and interpretted by trainers rather than operators
  * No need to explain how to perform a task, only note that it must be performed. "Change the blade" vs "Engage the spindle lock and rotate the locking night counterclockwise"

## For trainers

* Resources without a ✔ in the title are largely considered works in progress and may be incomplete
* ⚠️ Lines with a warning symbol should be delivered verbatim to the trainee and with extra emphasis. Usually a line is emphasised because we don't want a trainee to be able to claim they weren't provided the information later.

### Accessing

* Resources can be accessed via the [wiki](https://wiki.artifactory.org.au/en/docs/tool_inductions) (authenticated) or the [dedicated training offsite](https://train.artifactory.org.au) (Unauthenticated).

## For writers

* Editing is only possible through the wiki, not the offsite
* The offsite syncs every 5ish minutes, confirm it's updated before sending a link for feedback
* If a resource has a ✔ in the title it's largely considered stable. Discuss edits with stakeholders before making changes

> Avoid using formatted blockquotes like this - they don't render well on the training offsite
{.is-info}


### Document formatting

Unless otherwise required each resource should include:

* The lead trainer: Who trainers should go to when they need clarification on the resource. The lead trainer is a single point of contact for clear and consistent decisions and interpretations regarding the tool. In the interest of sharing volunteer load this doesn't need to be the absolute most experienced trainer.

`Lead: Xander McPudding`

* Who signed off on the resource: Ideally two trainers or experienced operators who can be consulted when changes need to be made. (One of which is usually the lead trainer)

`Signed off by: Xander, Preston`

* PPE table: Remove lines that aren't applicable

```
| Item  | Requirement | Notes  |
| - | - | - |
| Eye protection (impact/splash) | Y/M/N |  |
| Eye protection (EMR)           | Y/M/N | Be very specific as to what is needed. (wavelength and shade/OD) |
| Ear protection                 | Y/M/N | Include a sound rating if you can. |
| Gloves (general)               | Y/M/N | Note if gloves are specifically contra-indicated. I.e. bench grinder, mill, lathe. |
| Gloves (chemical)              | Y/M/N |  |
| Gloves (heat)                  | Y/M/N |  |
| Enclosed shoes                 | Y/M/N |  |
| Safety boots                   | Y/M/N |  |
| Mask/Respirator (dust)         | Y/M/N | Note required class of respirator cartridge. I.e. P1, P2, P3. |
| Mask/Respirator (vapours)      | Y/M/N | Note required class of respirator filter cartridge. I.e. A, B, E, K. (Typically ABE for general chemical filtration.) |
| Long sleeves                   | Y/M/N |  |
| Natural fibre clothing         | Y/M/N |  |
```

> Every time you use a numbered list just leave each number as `1.`, the system will render them as actual numbers and this way it's easier to add steps in the middle later on.
{.is-info}

* Materials/notes: In particular list out if specific types of material cannot be used
* Consumables: Note location and type of provided materials, whether personal consumables can be used, expectations around consumable replacements
* Prestart checks: Steps that are performed before using the tool, in most circumstances it should be safe to walk away at any point during this section.

```
Pre:

1. Ensure material and bit are appropriate
1. Set blade guard height
```

* Operating steps: Steps that are performed while using the tool. It's expected that when in this section the operator has 100% attention on the task at hand and performs a shutdown procedure before walking away. Usually this section will include actually powering up the equipment

```
Using:

1. Turn on the machine
1. Let the tool spin up completely before engaging
```

* Cleanup steps: Note any post operation safety considerations, what the cleanup procedures are, how to pack away the tool etc.

```
After:

1. Let blade cool before removing from tool
1. Cleanup includes: Bench, floor
1. Empty bin if over 1/2 full
```

* Advanced operation: A list of things that are possible with the tool but aren't within scope for the induction. Acknowledging them allows us to address things that may be included in inductions elsewhere but aren't within our workshpo. (blade changing etc)

```
Advanced operations: Unsupported cutting
```

### Complex topics

While we typically assume that trainers can speak to the nitty gritty of how to perform each step without detailed information there are times when an indepth explaination is required. You can add a specific titled section if needed but sanity check with another trainer beforehand.

eg. [Sawstop safety system](https://wiki.artifactory.org.au/en/docs/tool_inductions/wood#sawstop-safety-feature)

### Lines delivered verbatim

* So that operators can't claim that they didn't receive specific information you can add a warning symbol to steps or other information. The expectation is that these lines are delivered verbatim and with extra emphasis.

eg. [Sawstop safety system](https://wiki.artifactory.org.au/en/docs/tool_inductions/wood#sawstop-safety-feature) - Financial responsibility

`⚠️ Machine operators are financially responsible for all triggers. This includes the cartridge ($170+) and blade ($80-300).`