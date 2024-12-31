---
title: Vinyl cutter software setup
description: 
published: true
date: 2024-02-10T09:28:18.376Z
tags: 
editor: markdown
dateCreated: 2024-02-10T09:28:18.376Z
---

# Vinyl cutter software setup

> This information is for when a PC is being set up to use the vinyl cutter for the first time.
> Normal users do not need the information on this page.
{.is-info}

1. Install Inkscape.

        winget install Inkscape.Inkscape
    
2. Plug in the vinyl cutter (USB + power) and turn it on.

3. Check Device Manager for the COM port that the vinyl cutter is connected to. In the screenshot below, it's COM3.

    ![vinyl-cutter-device-manager.png](/tools/cnc/vinyl/vinyl-cutter-device-manager.png)
    
4. Load the vinyl cutter with a piece of vinyl for testing.

5. Open Inkscape.

6. Draw something simple (like a circle). Convert objects to paths, break apart, etc. as usual.

7. Go to Extensions -> Export -> Plot.

    ![vinyl-cutter-inkscape-1.png](/tools/cnc/vinyl/vinyl-cutter-inkscape-1.png)

8. On the "Connection Settings"tab, set the COM port to the one that you found in Step 3.

    ![vinyl-cutter-inkscape-2.png](/tools/cnc/vinyl/vinyl-cutter-inkscape-2.png)
    
9. Leave all the other settings on the "Connection Settings" tab as they appear in the screenshot.

10. Leave all the settings on the "Plotter settings"tab as they appear in the screenshot.

    ![vinyl-cutter-inkscape-3.png](/tools/cnc/vinyl/vinyl-cutter-inkscape-3.png)

11. Leave all the settings on the "Plot features" tab as they appear in the screenshot.

     ![vinyl-cutter-inkscape-4.png](/tools/cnc/vinyl/vinyl-cutter-inkscape-4.png)
    
12. Press "Apply" to start the cutting of your simple drawing. Check that it cuts successfully.
    
