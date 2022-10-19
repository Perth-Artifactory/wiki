---
title: Security Cameras
description: 
published: true
date: 2022-10-19T10:09:30.644Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:42:36.637Z
---

## Security Cameras

*This process applies to Ubiquiti cameras that connect to our NVR*

Set the camera to DHCP and configure static map via {pfsense} to

-   name: cam-\$location
-   IP: Select next in range using

Set the camera credentials to the ones found in the password database under Security.

Use the NVR to adopt the camera

Camera setup:

-   Record mode: motion
-   Quality: High
-   Seconds before/after: 10
