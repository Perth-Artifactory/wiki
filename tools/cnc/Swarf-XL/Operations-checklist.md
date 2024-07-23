---
title: Swarf XL / Swarf XL Operation Checklist
description: User instructions for the Swarf XL CNC router
published: true
date: 2024-07-23T09:56:24.780Z
tags: 
editor: markdown
dateCreated: 2024-07-22T04:59:37.567Z
---

> You need to be trained before using our CNC router.
>
> Only current, authorized trainers can deliver router training. Reading these instructions does not constitute training.
{.is-warning}

## CNC Router Safety 
### 1.	Personal Protective Equipment (PPE):
- Eye Protection: Wear safety glasses or goggles at all times to protect against flying debris.
- Respiratory Protection: Operate the machine with both the dust extraction and filtration systems enabled whenever possible. You may wish to use a dust mask or respirator rated for woodworking to prevent inhalation of wood dust particles.
- Ear Protection: The machine room is a noisy environment, especially with the router in operation. Use of ear protection is recommended.
- Clothing: Avoid loose clothing, jewelry, and tie back long hair to prevent entanglement.
### 2.	Machine Operation:
- Emergency Stop: Locate and know how to use the emergency stop button in case of any unexpected situations. Do not hesitate to use it.
- Clear Work Area: Ensure the work area is free from clutter to prevent interference during operation.
- Secure Materials: Always securely fasten materials to the bed of the CNC router using clamps or appropriate fixtures to prevent movement during cutting.
- Moving Parts: Be aware of moving parts such as the spindle and gantry. Keep hands clear of these areas during operation.
### 3.	Dust Management:
- Dust Extraction: Use the dust extraction system or a vacuum cleaner to capture wood dust at the source.
- Airborne Dust Filtration: Use the air filter when cutting wood or other materials that create airborne particulates. (Located above the power tools)
- Minimize Dust Exposure: Clean up dust promptly.
- Respiratory Protection: Wear a dust mask or respirator rated for woodworking to protect against inhalation of wood dust particles.
### 4.	Fire Safety:
- Fire Extinguisher: Know the location of the nearest fire extinguisher and how to use it.
### 5.	Electrical Safety:
- Do not open the machine electrical cabinet. 
- Do not operate the machine if you become aware of any electrical hazard such as broken or fraying wires. Isolate the machine and tag it “out of service” using the tags provided near the mill.
### 6.	Emergency Procedures:
- Injury: Report any injury, no matter how minor, to a member of the management committee and seek medical attention if needed.
- Do not operate the machine if the machine appears damaged or does not operate properly. Isolate the machine and tag it “out of service” using the tags provided near the mill.
### 7.	Training and Supervision:
- Only trained and authorized people should operate the CNC router. Reading these instructions does not constitute training. You can check your authorization status using the [Training Tracker](https://perart.io/check_training) tool on Slack. You must have a ✅ next to "Router (CNC/Swarf-XL)".
- Even if you are authorized, seek further instruction if you are unsure about any aspect of machine operation.

## Preparing for Operation
### 1.	Power On: 
Ensure the CNC router and the computer controlling it are powered on by switching on the isolator on the machine and then starting the computer via the button on the top right of the monitor.
- The CNC router requires a 15A supply. It is plugged into the 15A outlet next to the rear roller door via an extension cord. If the machine cannot be powered on then check the outlet.
- The isolator is on the left of the machine (seen from the operator’s position) at about knee height. There is a GPO on the machine that powers the computer and the chiller.
### 2.	Start the UCCNC software. 
After logging in to your user account, double-click the “UCCNC” icon to start the program.
- The program takes a few seconds to load and pre-compile. 
- If the program cannot locate the controller hardware and/or license file, a “demo mode” dialogue box will open.  
### 3.	Home (reference) the machine. 
You may wish to jog the machine close to the home position before homing, as the homing speed is significantly slower than the jog speed.
### 4.	Fit a spoil board 
If no spoil board is fitted, then fit one. If necessary you can laser cut your own using one of the templates here. Use of a spoil board is compulsory except where: 
- you are fixturing using a vise
- you are doing work where the depth of cut is small relative to the material (e.g. engraving, levelling a thick slab).
### 5.	Load Material 
Securely fix the material to the router bed. Make sure it is flat and firmly held down to prevent movement during machining. Common options for fixturing are:
- Strap clamps. Note these must be supported at the end not bearing down on the work, at approximately the same height as the work (+/-~2mm). Strap clamp bolts can be run into and out of the bed using an electric drill or driver but must be tightened by hand to prevent inadvertent over-tightening and damage to the bed.
- Toe clamps. Note that toe clamps are not required on all sides of the material: it is generally sufficient to have a clamp on one side and a solid block fixed to the bed on the opposite side. 
- A machining vice. The vice can be fixed directly to the bed and material placed in the vice. Note this method consumes a lot of available vertical travel and may not be suitable for all jobs. 
- Double-sided tape or adhesive. These methods must be used in conjunction with a spoil board. It is usually a good idea to cover both the surfaces to be adhered with masking (painter’s) tape, so the adhesive can be cleanly removed. If you use masking tape, make sure you rub it down firmly.
### 6.	Install Tool 
Select the appropriate cutting tool for your job (e.g., end mill, drill bit). Insert the tool into the router's spindle and tighten it securely using the collet and wrenches provided.
- Use only the appropriately sized collet. Each collet covers a very limited size range (typically 1mm) and any tool has one and only one correct collet. The indicated size is the largest size the collet will hold: an “8mm” collet will cover the range 8mm ≥ x > 7mm.
- Clip the collet into the collet nut before inserting the tool into the collet. The collet needs to compress to clip onto the nut and cannot do so with a tool installed. Installing the collet nut without the collet properly engaged will result in damage to the collet and nut.
- Tighten the collet nut securely, but do not over-tighten. The amount of pressure you can exert with 1-2 fingers on each spanner should be sufficient.
### 7.	Optional: Probe the Tool Length 
If your job requires more than one tool then you can save some time and hassle by using the probe to measure the length of each tool. If you are going to use this feature, then make sure you measure the length of the first tool before setting the workpiece origin.
- If the probe is not connected to the CNC router, then connect it. It plugs into the 4-pin aero-style connector on the side of the box underneath the emergency stop.
- Position the tool length probe on the CNC router bed in a clear area where the tool can be lowered without obstruction and jog the tool so it is over the probe. Any convenient position will do, so long as it will remain accessible throughout the job. The “Position 1” button in the UCCNC user interface will move the tool to the x=21mm, y=31mm position, which coincides with the probe centre when the probe is in the corner of the bed closest the emergency stop.
- Click the “Probe” button in the UCCNC user interface. The tool should descend until it touches the probe, retract slightly, and descend again at a lower speed. If you wish you can verify that the tool length has been set correctly by checking the tool offset value in the “Offsets” tab of the UCCNC UI. The value should approximately equal the length of tool sticking out of the collet.
## Setting Workpiece Origin
### 1.	Set X and Y Coordinates
- Move the tool to the desired starting point. This can be anywhere but if the job is large relative to the material (or to the work envelope of the machine) it is important that it is consistent with the origin specified in the CAM stage of the design.
- If precise location relative to the edges of the stock is required, then nudge the tool towards the work and ‘touch off’. The exact point of touch can be found either by listening for contact between the tool and the work (with the spindle on), or by feeling for contact while gently rotating the tool back and forth by hand (with the spindle off, obviously). 
- Use the CNC software to set the X and Y zero reference. If touching off, do one axis at a time and remember to compensate for the radius of the tool. Note that the axis DRO value can be set either by zeroing, or by entering a numerical value in the “work coordinates” box and pressing “enter” (important!).
### 2.	Set Z Coordinate
- Move the tool to the desired starting height. This can be anywhere but should be consistent with the origin specified in the CAM stage of the design.
- If precise location relative to the top of the stock is required, then nudge the tool towards the work and ‘touch off’. The exact point of touch can be found either by listening for contact between the tool and the work (with the spindle on), or by feeling for contact while gently rotating the tool back and forth by hand (with the spindle off, obviously). Feeling for contact can be done with a piece of paper, feeler gauge or other reference material on top of the work if desired, but remember to compensate for its thickness.
- Use the CNC software to set the Z zero reference.

## Loading and Running CNC Programs
### 1.	Load Program (G-code) 
Load the G-code file generated from your CAD/CAM software into the UCCNC software using the “load file” button.
### 2.	Inspect Tool Path 
- Visually inspect the tool path graphic in the UCCNC UI. Check that the design origin corresponds to the origins you have set for the workpiece. Check that any fixtures are well clear of the tool paths shown.
- If desired, run the job with the workpiece z-axis origin set higher than the true value so that the machine “cuts air”. This method is useful if fixturing options are limited.
### 3.	Fit and start Dust Extraction
- Install the dust shoe on the spindle. Ensure that the blast gate for the machine is open and all other unused blast gates are closed.
- Start the dust extractor.
- Start the dust filter if your job will create airborne particulates.
### 4.	Run Program
- Execute the program through the UCCNC software user interface. Note you may have to click “cycle start” a second time as tool change commands will result in UCCNC waiting for confirmation a manual tool change has been made.
- Monitor the initial movements to ensure the tool moves correctly and doesn’t collide with the material or fixtures.
### 5.	Adjust Cutting Parameters if necessary
- The feed rate and spindle speed will be set in the G-code program as part of the CAM phase of your design. They can be adjusted in the UCCNC user interface at any time. 
- Deciding to override feed and speed should be done based on observation of the machine in operation.
### 6.	Monitor Operation
- Throughout the operation, monitor the cutting process to ensure everything is proceeding as planned.
- Be prepared to pause the operation (“feed hold” in the UCCNC UI or the blue button on the machine) or stop the operation if necessary. Non-emergency stopping can be done using “cycle stop”. If necessary, don’t hesitate to use the Emergency Stop button.
## Post-Operation
### 1.	Inspect Workpiece 
Once the CNC router has finished, inspect the finished workpiece for quality and accuracy.
### 2.	Remove Material 
Carefully remove the machined material from the router bed.
### 3.	Shutdown:
- Move the spindle to a position that will facilitate cleaning the machine.
- Shut down the computer.
- Power off the CNC router at the isolator.
- Clean the router bed and workspace and return all tools and fixtures to their proper locations.
## When things go wrong
### 1.	UCCNC reports alarms 
The controller monitors for several trouble conditions and reports alarms through the UCCNC user interface. In each case the machine will be placed in “offline mode” and a text box will open to instruct the user how to clear the alarm:
- Drive faults. In the event of a drive fault the machine will stop operation and retract the tool (if the z axis is not the faulted drive). Drive faults can be cleared by cycling the power to the drives by triggering the emergency stop hardware button for a few seconds then turning off “offline mode” through the UCCNC user interface. The machine will need to be re-homed afterwards. 
- Chiller fault. The chiller will normally be powered on when the machine is turned on but if the chiller reports a fault or is not powered, the CNC router will raise an alarm. Once the issue is resolved, “offline mode” can be turned off and operation resumed.
- VFD fault. If the spindle variable frequency drive (VFD) reports a fault, the CNC router will raise an alarm. Once the issue is resolved, “offline mode” can be turned off and operation resumed.
- Probe over-travel. If the tool length probe does not trigger on first contact with the tool, it may report over-travel. If the probe has been accidentally pressed outside a normal probing operation, no action is required to clear the fault besides turning off “offline mode”. If the fault occurred during tool length measurement, then do not use the probe further and report the issue in [#cnc-router](slack://channel?team=T0LQE2JNR&id=C07DDHBALCB) on Slack.
### 2.	Accidentally triggering limit switches 
If the machine is moved beyond its limits a physical limit switch will be triggered and the machine will be placed in a “reset” condition. To recover from this situation:
- Click the “override limits” button in the UCCNC user interface. This will tell the controller to temporarily ignore the limit switches.
- Click the “reset” button in the UCCNC user interface.
- Move the machine away from the triggered limit using the jog controls. Be very careful to move in the correct direction.  
### 3.	Resuming a stopped program 
It is sometimes necessary to stop a job and re-commence it part way through - typically if you have activated the emergency stop. Provided the machine was homed before starting the job, it is generally possible to resume with minimal ill effects:
- Deal with whatever problem led to you stopping the job.
- If necessary, re-home the machine. All axes are changed to un-homed status when an emergency stop is triggered. Otherwise you can check the homed status of each axis in the UCCNC user interface.
- Find the point in the G-code program from which to resume. Generally this should be a few lines prior to the line of code being executed when the job was stopped. Make sure the line is selected in the UCCNC user interface.
- Jog the machine to a safe location. This should be a location where the tool can move in a straight line to the part of the job where operation will be resumed without hitting fixtures or stock.
- Click “Run from here”. UCCNC will run through the entire program to that point to calculate what the state of the machine should be when it resumes. A dialogue box will open displaying the details of the move required to get to the resume point.
- Verify that the required first move will not bring the tool into contact with any fixture or material. 
- Click to confirm the first move. When the machine has executed the move, click “cycle start” to resume the job.
### 4.	Damage to the machine / unexplained problems 
If the machine is damaged or seems to be operating abnormally, do not attempt to repair it. Report the issue in [#cnc-router](slack://channel?team=T0LQE2JNR&id=C07DDHBALCB) tag it as “out of service” using the tags provided near the mill.
