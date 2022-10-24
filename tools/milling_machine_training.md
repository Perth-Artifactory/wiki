---
title: Milling Machine Training
description: 
published: true
date: 2022-10-19T12:48:36.051Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:59:08.991Z
---

# Milling Machine Training

This page sets out the general content for training of new milling machine users. It is intended for an audience of trainers and users who have completed training (but might need reminding on some points). **Reading this page is not a substitute for being trained.** Training includes a meaningful amount of hands-on time with the machine and can't be done on the internet.

## Agenda

Training would typically cover:

-   Introduction of trainer and participants
-   Overview of Artifactory policies related to the milling machine
-   Basic anatomy and operation of the machine
-   Overview of tooling
-   Principal safety issues and their mitigation
-   Participants make a small project. Ideally the project allows exposition of:
    -   Work-holding
    -   DRO operation
    -   Facing, peripheral milling, drilling
    -   Feed and speed selection
    -   Edge finding
    -   Precision
-   Typical work cycle including machine startup and shut down
-   Feedback and discussion of next steps

```{=html}
<!-- -->
```
    ===== Overview of milling machines =====
    *   In a lathe, the cutting tool stays still and the workpiece moves. In a mill it’s the other way around. The workpiece is securely fixed to the table and the tool is fastened in the spindle, (like in a drill press, but with some important differences).
    * The tool can interact with the workpiece in a range of different ways, for example:
      * Peripheral milling, where metal is removed alongside the cutter and the cutter moves in the x/y plane
      * Facing, where metal is removed beneath the cutter and the cutter moves in the x/y plane
      * Drilling / boring, where the tool moves in the z direction
      * Slitting
      * Even scraping!
    * Some typical milling tools:
      * End mill
      * Facing cutter
      * Drill bit
      * Slitting saw
      * Boring bar
      * Fly cutter

## Anatomy of the milling machine

-   The table sits on the saddle which sits on the knee which hangs on the column.
-   The table moves on the saddle to create x motion
-   The saddle moves on the knee to create y motion
-   The knee moves on the column to create z motion
-   The head is mounted on the ram which is attached to the turret. These are not moved unless there is a specific need.
-   The head contains the mechanisms to move the quill and the spindle.
-   The tool is mounted in the spindle.
-   The spindle and tool rotate.
-   The quill moves the spindle and tool in the z direction. Thus the mill has two independent ways of creating z-motion between the tool and workpiece
-   The mill has the following secondary systems:
    -   A pneumatic powered drawbar to assist with tool changing
    -   A lubrication system
    -   A coolant circulation system (not normally in use)
    -   A digital readout (DRO) to track the position of the table and quill in 3 dimensions.

## Control of the milling machine

-   All the linear motions can be done manually
    -   The table can be moved in x, y and z using the handwheels
    -   The quill can be lowered using the handle or the micro-feed wheel, but the head controls need to be correctly set to do it
-   All linear motions can be powered (normally)
    -   The table can be power-fed at variable speed in the x direction (and, when the mill is fully functional, the y direction). The speed is controlled by a VFD and the user adjusts it with a feed speed control knob.
    -   The table can be moved in the z direction but cuts cannot be made by such movements
    -   The quill can be power-fed, within limits. This topic is covered separately.
-   All axes can be mechanically clamped to prevent motion.

## Safety

The **key hazards** associated with the machine are:

-   Contact with revolving tools
-   Long hair, loose clothing or jewellery becoming entangled in the moving parts of the machine
-   Work pieces, broken cutting tools, swarf etc being ejected from the machine
-   Electric shock
-   Closing movements of parts under power can result in finger trapping
-   Closing movements between the table and fixed structures can result in body crushing
-   Heavy objects such as vices and index fixtures can fall from the table
-   Sharp edges on cutters, work pieces and swarf can cause cuts
-   Contact with cutting fluids, oil and grease can irritate skin
-   Accidental starting of the machine
-   Lack of sufficient space around the machine can lead to the operator being pushed by passers by resulting in injury
-   Slippery floors or loose items around the machine can cause slips that result in contact with the moving parts of the machine
-   Manual handling of heavy items such as vices and index fixtures can be a hazard

They key **risk mitigation measures** in place are:

-   The machine can be electrically isolated and locked out when not in use. Only authorised users are informed of the combination
-   The machine is provided with and emergency stop.
-   All cabling is armoured to protect it from damage.
-   Except during training, people other than the operator are not permitted inside the working area when the machine is in operation
-   The floor surface must be kept free of spills, loose items and swarf.
-   The operator and any trainees must wear eye protection at all times when within the working area
-   The operator and any trainees should consider wearing ear protection when the machine is in operation
-   Substantial, non-slip, flat-heeled shoes that cover the whole of the foot, must be worn when using any machine.
-   Long hair and loose clothing must be secured and dangling jewellery must not be worn when operating the machine.
-   Gloves must not be worn when using the machine, although they are permissible for manual handling when the machine is not in use.
-   Manual handling tasks associated with changing heavy vices and indexing heads etc should be assessed prior to commencing, and assistance sought if necessary.
-   The machine must be electrically isolated before any internal mechanisms are adjusted.
-   Cutters must be stopped when positioning the work piece, clearing swarf, adjusting coolant pipes, measuring or gauging.
-   Hands must be kept well away from the table when it is traversing under power to minimise the risk of trapping fingers.
-   Coolant nozzles must not be adjusted whilst the machine is in operation.
-   Swarf must never be removed whilst the machine is in operating.
-   Suitable implements must be used to remove swarf. Avoid hands coming into contact with swarf.
-   Contact of metal work fluids with the skin should be minimised. Barrier cream is available.
-   Wash hands thoroughly after the use of metalworking fluids.

## Tool holding

The tool mounts in a tool holder which attaches to the spindle via a taper.Common tools and tool holders include:

-   Collets and collet chucks can mount any tool with a cylindrical shank within their size range. This is the usual solution for mounting end mills. This mill uses ER40 collets, which go up to 25mm.
-   An arbor is used to mount Indexable face mills, slitting saws and a range of other tools. ‘Arbor’ is a generic term and not all arbors fit all tools.
-   A boring head is used to mount boring bars.
-   A drill chuck can be used to mount twist drills.

## Work holding

The workpiece must be securely fixed to the table, both for functional and safety reasons. Common ways of doing the fixing include:

-   In a vise that is itself securely fixed to the table. A precision vise that is aligned to the axes of the machine can make work setup easier too – more on this later.
-   Using the hold down set and the t-slots in the table.
-   Special fixtures can be made to solve hold-down problems not addressed by the above.

## Head controls

Controls available on the head include:

-   A manual spindle brake to stop the rotation of the spindle after the motor is turned off.
-   A two-position speed range selector to set the available range of spindle speed. Fine control of spindle speed is done electronically by the spindle motor’s variable-frequency drive.
-   A range of controls for moving the quill. The quill has three movement modes:
    -   Basic manual control using the quill handle and, optionally, the depth stop, that resembles the movement of a drill press.
    -   Fine manual control using the fine-feed wheel
    -   Powered quill feeding using the quill feed selector to select the feed rate, the quill feed direction selector to select the feed direction, and optionally the depth stop to automatically disengage the feed when the correct depth is reached. The quill drive train is relatively delicate and not suitable for high-power operations such as twist-drilling large holes.
-   The quill movement mode is set by a combination of the quill feed engagement and the clutch:
    -   Any time the clutch is disengaged, the machine is in *basic manual mode*.
    -   When the clutch is engaged and the quill feed is disengaged, the machine is *fine manual control*.
    -   When the clutch and quill feed are both is engaged, the machine is in *powered quill feeding mode*.

## Digital Readout (DRO)

-   The DRO shows the position of the table and the quill. The x, y and z axes are for the table. The a axis is for the quill.
-   The DRO does not show absolute position: all the axes can be zeroed at any point.
-   Somewhat confusingly, the DRO can manage two independent zero positions, called ABS (absolute) and INC (incremental). Pushing the ABS/INC button switches between them. The typical use is to use ABS to locate features on the workpiece, and INC to machine the features.
-   The DRO has a lot of features. The most useful ones are:
    -   ‘1/2’ function, for zeroing an axis on the centreline of the workpiece
    -   Circular pattern function
    -   Linear pattern function

## Machining parameters (feeds and speeds, tool choice, lubrication)

The quality of the cut and the speed with which your job is completed depend critically on the tool you use, how fast it turns, how fast you feed it into the workpiece, and what, if anything, you lubricate it with.

#### Tool selection

-   There is a cost / quality / time trade-off to be made here. Generally we want good (or acceptable) quality; we don’t want to spend too much on tooling; and we don’t need maximum material removal rate.
-   Using the example of end mills, very simplistically:
    -   Use the largest diameter tool that will do the job (or that you can afford)
    -   Use carbide end mills (as opposed to high-speed steel) if you can afford them. Ideally use coated carbide for steel and uncoated for aluminium. If you want one tool to do both, make it uncoated.
    -   Use four flute end mills for steel and 3 or 2 flute end mills for aluminium.

#### Feed rate and cutting speed

-   Ultimately the factors that affect cutting forces, and hence the quality of the result, are:
    -   The depth of cut, or how much of the cutter’s length is contacting the workpiece at one time, controlled directly by the operator
    -   The degree of engagement (‘stepover’), or how much of the cutter’s circumference is contacting the workpiece at one time, controlled directly by the operator
    -   The chip load, or how large a radial ‘bite’ each tooth of the cutter is taking, determined by spindle speed, feed rate and number of flutes of the tool.
    -   The surface speed, how fast the tool is moving against the workpiece, determined by spindle speed and tool diameter
-   There is a lot of reference material and some good online tools for choosing machining parameters. Mostly though, we have the tools we have and we just want to pick the right spindle speed, stepover, depth of cut and feed rate.
-   The table below shows some recommended surface speeds and chip loads for common tools and materials:

#### Lubrication

-   The machine has a pumped cooling system. We don’t use it because it is messy.
-   Cut steel using oil, preferably cutting oil
-   Cut aluminium using kerosene or WD-40

## Precision

-   The machine is capable of working to precise dimensions, of the order of 0.025mm or less, but achieving that precision requires precise setup and careful machining.
-   ‘Precision’ means different things to different people. For hobby machining work one of the first places you are likely to encounter a need for a particular degree of precision is with fits, which might require a dimension window of 0.0005 to 0.001 inches (0.0125 to 0.025mm). That sounds difficult but is quite achievable on the machines we have.
-   General strategies for precision setup include:
-   Direct measurement of runout using dial and test indicators
-   Exploiting the geometry of high-precision tools and fixtures, such as vises, parallels and angle plates.
-   It is not compulsory to work to the ultimate precision of the machine. You only need as much precision as you need.
-   The head and vise need to be kept trammed for the machine to be capable of precise work. They can move if the machine is crashed.
-   This is a very big topic and way beyond what we can cover here.

## A typical usage cycle

-   Work environment:
    -   Clear yourself a work space if necessary, turn on the lights.
    -   Make a quick inspection of the mill. Did the previous user clean up? How are the head controls set?
-   Get the machine ready
    -   Unlock the isolator and turn the power supply on.
    -   Unlock the tool cabinet.
    -   Switch on the compressor with the air connection to the machine detached. When the compressor is pumped up, plug the air line in.
    -   Give the oiler a pump (when it's installed)
-   Fix the workpiece
    -   If necessary, mount and tram a vise. (Tramming is the process of aligning the vise’s precision surfaces to the axes of the mill).
    -   Securely fasten the workpiece, aligning it if necessary
-   Mount the tool in the tool holder
    -   Process will vary according to the tool. Generally this should be done with the tool holder out of the mill
    -   For mounting end mills in a collet chuck:
        -   ensure both the collet and the mill shank are clean and degreased. Spinning the tool in the collet can damage the collet and reduce its precision.
        -   The collet needs to be snapped into the nut before the tool is inserted
        -   The tool should be inserted as far into the collet as possible, ideally 2/3 the length of the collet
        -   The collet chuck should be done up tight (175 NM) in the tool setting station using the correct tool.
-   Mount the tool holder in the mill
    -   Align the driving dogs with the slots in the tool holder
    -   Activate the power draw bar to capture the tool holder. FINGER TRAP HAZARD!
    -   Note the power draw bar only works with the quill in the raised position.
-   Zero the DRO
-   Select spindle speed and feed rate
    -   Select the appropriate spindle speed range with the speed range selector.
    -   Set the desired spindle speed with the spindle speed control.
-   If power feeding, set the feed speed with the feed speed control.
-   Perform the machining operation
    -   Set the tool position for the desired depth and breadth of cut
    -   Take a test cut if necessary
    -   Make the cut, either manually or with the powered feed
    -   Repeat until the operation is complete
-   Remove the workpiece from the mill
-   Either do other machining operations or remove the tool holder from the mill and the tool from the tool holder.
-   Clean up swarf using a brush or vacuum cleaner
-   Put away tools
-   Power off the mill, lock the isolator and the tool cabinet.
