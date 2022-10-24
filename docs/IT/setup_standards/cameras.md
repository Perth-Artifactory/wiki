---
title: cameras
description: 
published: true
date: 2022-10-19T11:36:59.913Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:43:40.422Z
---

All artifactory secruity cameras are setup to the following specifications

## Security Cameras

*This process applies to Ubiquiti cameras that connect to our NVR*

Set the camera to DHCP and configure details via {pfsense} to

-   name: cam-\$location
-   IP: IP LIST

Set the camera credentials to the ones found in the IT KeePass database under Security.

Use the NVR to adopt the camera

Camera setup:

-   Record mode: motion
-   Quality: High
-   Seconds before/after: 10
