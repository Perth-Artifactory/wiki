---
title: Web Server
description: 
published: true
date: 2022-10-19T11:36:53.833Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:43:31.500Z
---

# Web Server

## System Details

| HOSTNAME   | web.internal.artifactory.org.au |
|------------|---------------------------------|
| IP Address | 10.60.210.64                    |
| VM CPU     | Single Core                     |
| VM RAM     | 1GB                             |
| VM DISK    | 20GB                            |
| Services   | Website                         |

## Service Details

\* (added 2015-09-15) - space.artifactory.org.au webroot now contains spaceapi.json - which is the endpoint for spaceapi. It's not updated automatically yet -- needs door2.0 -- however it now makes the space visible with apps such as 'myhackerspace'

\* camera snapshots - There is a cron job (/root/scripts/cam_loop.sh) that grabs a snapshot from each camera every minute and saves the last 10 in space.artifactory.org.au/cameras/name/
