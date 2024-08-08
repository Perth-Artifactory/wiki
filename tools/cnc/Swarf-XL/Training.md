---
title: Swarf XL Training
description: How to get training for Swarf XL
published: true
date: 2024-08-08T11:48:54.684Z
tags: 
editor: markdown
dateCreated: 2024-07-23T09:07:49.480Z
---

> You need to be trained before using our CNC router.
>
> Only current, authorized trainers can deliver router training. Reading these instructions does not constitute training.
{.is-warning}

## Training Overview 
Training for Swarf XL has two phases: 
- CAD / CAM training, which is computer-based and covers the process to the point where a G-code file for use on the machine has been produced 
- Machine Operation, which is conducted hands-on with the machine. During this phase of the training the file produced in CAD / CAM Training is used to make a part.

CAD stands for Computer Aided Design. In the context of using the machine, CAD involves generating a digital representation of the thing you want to make. You may be able to make things from CAD models you have downloaded but we teach the very basics anyway.

CAM stands for Computer Aided Manufacturing. In this context, CAM involves generating instructions from a CAD model that tell the machine how to make it. Since those instructions are particular to the machine, materials, cutting tools available and of course what you want to make, it is generally not possible to bypass the CAM step and just download something from the internet.

### Software Tools
We teach two different CAD / CAM tools and workflows. Feel free to choose the one that best suits your needs: 
- Aspire, a product of Vectric, is an excellent and easy to use 2d design program with good native CAM support for laser cutters and CNC routers. It is not free, but the Artifactory has a full Aspire license and the program can import vector files in a wide range of formats. Aspire suits CNC router users who want to make relatively simple parts (profiles cut out of sheet material for example) with limited time spent learning new software.
- Fusion (formerly Fusion 360) is a product of Autodesk. Fusion is a very flexible and powerful 3D CAD / CAM application with a deep feature set and a mountain of on-line instructional content. There is a "Personal Use" version that is free and highly capable. Fusion suits users who want to make 3-dimensional parts, learn a more powerful design tool, and/or go beyond the basics of CNC machining. However it requires a larger investment of time.   

### Prior Experience
If you have relevant prior experience, you are free to skip CAD / CAM training. The trainer will take a look at your work as part of Machine Operation training (as they would do for any trainee) and ensure it is OK to use on the machine.

## CAD / CAM using Fusion 
CAD / CAM training using Fusion is video-based and self paced. There is excellent instructional content on Fusion available on Autodesk's website (as well as independent content on YouTube). In addition, we have produced a video that shows specifically how to prepare a job for our CNC router using Fusion.

### Downloading and installing Fusion
The product you need to download and install is "Fusion for Personal Use"". (You will need to create an Autodesk account). Follow the link [here](https://www.autodesk.com/au/products/fusion-360/overview?term=1-YEAR&tab=subscription) and scroll down about 80% of the way, then click "Get Autodesk Fusion for Personal Use" and follow the prompts.

### General Instructions for Fusion

We recommend the following videos:

From the Ïntroduction to Fusion series (around 25 minutes total):
[Introduction to Fusion](https://help.autodesk.com/view/fusion360/ENU/courses/AP-GET-STARTED-OVERVIEW)
[User Interface Overview](https://help.autodesk.com/view/fusion360/ENU/courses/AP-USER-INTERFACE-OVERVIEW)
[Set Preferences](https://help.autodesk.com/view/fusion360/ENU/courses/AP-SET-PREFERENCES)
[Adjust Display Settings](https://help.autodesk.com/view/fusion360/ENU/courses/AP-ADJUST-DISPLAY-SETTINGS)

From the Getting Started with Modelling series (around 40 minutes total): 
[Components and Bodies](https://help.autodesk.com/view/fusion360/ENU/courses/AP-BODIES-COMPONENTS-GS)
[Sketching Basics Overview](https://help.autodesk.com/view/fusion360/ENU/courses/AP-INTRO-SKETCH-BASICS-OVERVIEW)
[Sketch Constraints](https://help.autodesk.com/view/fusion360/ENU/courses/AP-INTRO-SKETCH-BASICS-CONSTRAINTS) 
[Extrude Solid Bodies](https://help.autodesk.com/view/fusion360/ENU/courses/AP-INTRO-SKETCH-BASICS-CONSTRAINTS)

If you want to use Fusion and are having problems with the video instruction, please feel free to ask for help in [#cnc-router](slack://channel?team=T0LQE2JNR&id=C07DDHBALCB).

### Specific instructions for using Fusion with Swarf XL
*to come*

It is recommended you download and install the assets below for Fusion. You can do this by selecting the "Manufacture" workspace and from the "Manage" section of the ribbon, selecting "Tool Library" and "Machine Library" in turn, then clicking the "import" icon and selecting the  file you just downloaded.
[Swarf XL starter wood tools library for Fusion](/artifactory_-_swarf_xl_-_wood_1.tools)
[Swarf XL / UCCNC post-processor for Fusion](/uccnc_swarfxl.cps)
[Swarf XL machine profile for Fusion](/artifactory_swarf_xl.mch)
## CAD / CAM using Aspire
CAD / CAM training using Aspire is conducted one-on-one and in person. The trainer will introduce the software and walk through all operations necessary to produce the machine instructions (G-code file) for a simple project. The "standard project" is a wooden sign engraved with text of the trainee's choice. If you would like to do something different for your training project, discuss it with your trainer.     

CAD / CAM training using Aspire can be requested in #training-and-inductions.

## Machine Operation
Machine Operation training is conducted one-on-one and in person. The trainee should arrive for training either: 
- Having completed CAD / CAM training,  or
- With simple project they have created as evidence of prior competency. Both the CAD design (in either Vectric or Fusion format) and the G-code are required. The project chosen should have simple fixturing and be able to be completed in under 30 minutes of machining time.

An outline of the material covered in Machine Operation training is [here](/tools/cnc/Swarf-XL/Operations-checklist).

Machine Operation training can be requested in #training-and-inductions.
