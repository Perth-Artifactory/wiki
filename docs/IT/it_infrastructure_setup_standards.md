---
title: it_infrastructure_setup_standards
description: 
published: true
date: 2022-10-19T10:09:11.827Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:42:10.048Z
---

Hardware and Software Setup Standards

[Security Cameras](/subcommittee/it_infrastructure/setup_standards/cameras)

Access is based on a hierarchical system. If a tier has access to a server it is assumed that tiers above that also have access unless otherwise stated.

Order:

1.  Members
2.  IT Subcommittee
3.  Specific Officeholders
4.  IT Officer

# Servers

Unless otherwise noted auth is controlled by Userify.

## Core

| Use      | Used for general Unix access to the space. Can also be used for tunneling if desired. |
|----------|---------------------------------------------------------------------------------------|
| SSH      | Members+                                                                              |
| Root     | IT Subcommittee+                                                                      |
| OS       | Ubuntu 18.04                                                                          |
| Hostname | newcore                                                                               |

Notes:

-   Port forwarded to XXX

## Filer

| Use      | Runs the SMB share available in the space |
|----------|-------------------------------------------|
| SSH      | IT Subcommittee+                          |
| Root     | IT Subcommittee+                          |
| OS       | Ubuntu 18.04                              |
| Hostname | filer                                     |

Notes:

-   32G sda (OS), 750G sdb (files, /mnt/shared)
-   Running SMB

## NVR

| Use      | Records footage from the security cameras |
|----------|-------------------------------------------|
| SSH      | Specific Officeholders                    |
| Root     | Specific Officeholders                    |
| OS       | Ubuntu 14.04                              |
| Hostname | nvr                                       |

Notes:

-   32G sda (OS), 750G sdb (footage, /mnt/footage)
-   Running UniFi Video 1.3.5 as unifi-video

# Misc

## UniFi Video

The UniFi Video installation hostname is **NVR** and is listening via https on 7443 User accounts are created individually, contact the IT officer if you believe you should have access.

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
