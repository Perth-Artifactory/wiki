---
title: vcarve_instructions
description: 
published: true
date: 2022-10-19T12:45:43.385Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:55:07.972Z
---

{{ :process_guide:cnc-westozy-08.jpg?direct&100\|===== VCarve Instructions =====

<img src="/process_guide/vcarve_letter_t_animated.gif" class="align-right" />

\*\* \~\~ THESE INSTRUCTIONS ARE UNFINISHED \~\~ \*\*

*Contributions Welcome!*

...

VCarve is the supported software for use with Swarf-O-Mat.

This software is installed on the computers available in the computer room in the space.

Artifactory members can make a folder on the network that can be accessed by Swarf-O-Mat.

VCarve is kind of compatible with a range of vector formats but YMMV.

### Existing Tutorials

There are materials and video tutorials on how to use VCarve online. It's well worth checking these out.

[VCarve official 'How To' guides](http://www.vectric.com/WebSite/Vectric/support/support_how_to.htm)

[VCarve text and video tutorials](http://www.vectric.com/WebSite/Vectric/support/aspire3_vcp6/aspire3_vcp6_tutorials_tut.html)

### VCarve Local Specifics

We recommend going through the official instructions and tutorials thoroughly.

There are some speficica

##### Open VCarve

If you're using the computers in the computer room there should be a link on the desktop.

![](/process_guide/crv_icon.jpg)

##### Create new VCarve project

"Create new project", there is a link on the left hand side.

<img src="/process_guide/swarf-o-mat_splash.jpg" width="350" />

##### Set the dimensions of your new VCarve project

<img src="/process_guide/swarf-o-mat_new-bar.jpg" class="align-left" width="300" />Take care here.

It is important that you have a good visualisation of what your project will look like such as:

\* the dimensions of base material \* how your project will be carved out

**Size/Material**

Specify the material you will be using

Make sure the piece will fit comfortably within the material with enough of a border that you can clamp down and prevent the work from moving.

-   Width(x): 440mm
-   Height(y): 580mm
-   Thickness(z): 60mm

(Actual machine area: 460x600x70, but need to allow space to affix job.)

**XY Position**

This can be set to whatever, though local convention is to leave it to default.

That is to leave set it to: **bottom left**

##### VCarve

<img src="/process_guide/swarf-o-mat_blank.jpg" class="align-left" width="275" />

Congratulations! You now have a blank bit of material.

You can now arrange your job on the material and draw the **toolpaths** for your job.

These paths are **vectors** and map out the route that the Swarf-O-Mat will take to cut out your job.

<img src="/process_guide/vcarve_vectors-draw.jpg" class="align-left" /> <img src="/process_guide/vcarve_vectors-close.jpg" class="align-right" />

The **"Create Vectors"** are the main tools you will use to draw your project.

Make sure all the shapes are closed vectors (there are a couple of ‘join’ options, eg: select two lines, press \[j\] or by using the **"Join open vectors"** buttons.)

Useful: \[N\] for Node edit

What you need to be thinking while you are creating your project is **what path is the cutting tool taking?**

Are there multiple cuts? Are you cutting **on** the line as opposed to inside or outside the vector line? Are you cutting all the way through?

**NOTE:** usually do you NOT cut from the edge of your material using a milling machine. You usually place your job in the middle of a piece of material so you have **ample room to clamp your material to the milling machine deck**. Bear this in mind while drawing the necessary vectors on your material.

Once you are confident you have drawn a logical cutting path for your whole job you need to specify this path to VCarve using \`Toolpaths\` -- the right hand side pop-out options menu.

------------------------------------------------------------------------

<img src="/process_guide/vcarve_pin.jpg" class="align-left" width="275" /> <img src="/process_guide/vcarve_toolpaths-2.JPG" class="align-right" />

##### Toolpaths

Make a toolpath for each logical cut your job makes.

For example, if you were making a bas-relief of a particular size you would use 2 toolpaths:

\~ one toolpath to cut out the job from the material  
\~ one toolpath to engrave the material

There are several cutting options. The most commonly used are:

\[profile\] cuts out a shape;  
\[pocket\] removes a pocket of material;  
\[drill hole\] drills a hole (!)

You need to create each path individually. Try and think through your job so that you can put the paths in logical order.

(Note: you can use the \`pin\` in the top right hand corner to stop this toolbar from popping closed.)

<img src="/process_guide/vcarve_toolpaths-bit.JPG" class="align-right" /> When you first create a path you need to set certain options.

**Cutting Depths** -- You should know how deep you require the cut to be.

If you are actually cutting a piece out add a bit so that you can be sure it cuts all the way through (eg for 3mm thick material you would set this to 3.2mm to cut all the way through **BUT YOU MUST ADD BUFFER MATERIAL UNDERNEATH YOUR JOB IN THIS CASE**).

Obviously if you are creating a pocket or engraving you set the depth of the engraving (eg 1mm deep writing in 3mm thick material).

**Tool** -- if you are not familiar with bits **PLEASE SEEK ADVICE ABOUT THIS** so you can know what is the most appropriate bit for your job.

(Passes are calculated automatically)

**Machine Vectors** -- you will hopefully have a good idea of what is the best vector for your job.

If you are entirely cutting out one piece from another (a very common usage) use 'tabs' to keep your work steady.

VCarve tends to put them in weird places, particularly corners -- move them to appropriate positions (out of awkward corners, evenly spaced). Eg: for Jarrah decking: tabs 5mm long, 3mm thick.

Tips: Small bits carving aluminium get pushed around during pockets so that you end up with a ‘V’ shape/slope in profile. Solution: 2 tool paths: profile, then pocket. Skot’s favourite tool for jarrah and ply: 6mm end mill 3mm passes 24,000 rpm (slight risk of burning jarrah); acrylic: 12,000 rpm for not melting feed rate: 1300mm/min plunge rate: 600mm/min ramp plunge moves \[√ \] safe Z = clearance above the wood and clamps

Save Gcode (select all) Mach3 Arcs mm txt}}

![](/process_guide/vcarve_all-toolpaths.JPG)
