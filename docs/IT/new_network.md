---
title: Network Rebuild 2012
description: 
published: true
date: 2022-10-19T11:36:10.028Z
tags: 
editor: markdown
dateCreated: 2022-10-17T16:42:27.684Z
---

# Network Rebuild 2012

## Services on VMM0

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Service</th>
<th style="text-align: left;">Software</th>
<th style="text-align: left;">VM</th>
<th style="text-align: left;">Responsible</th>
<th style="text-align: left;">Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">LDAP SSO</td>
<td style="text-align: left;">OpenLDAP</td>
<td style="text-align: left;">core</td>
<td style="text-align: left;"><a href="/user/southen">southen</a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">DHCP</td>
<td style="text-align: left;">ISC DHCPd</td>
<td style="text-align: left;">core</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">DNS</td>
<td style="text-align: left;">ISC Bind</td>
<td style="text-align: left;">core</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Potential for LDAP as backend.</td>
</tr>
<tr class="even">
<td style="text-align: left;">External SSH</td>
<td style="text-align: left;">OpenSSH</td>
<td style="text-align: left;">shell</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Wiki</td>
<td style="text-align: left;">Apache + DokuWiki</td>
<td style="text-align: left;">web</td>
<td style="text-align: left;"><a href="/user/prd">prd</a></td>
<td style="text-align: left;">Template-based, potentially derived from <a href="http://demo.interarma.org/wikibundle">http://demo.interarma.org/wikibundle</a></td>
</tr>
<tr class="even">
<td style="text-align: left;">Scheduler</td>
<td style="text-align: left;">Apache + PhpScheduleIt2</td>
<td style="text-align: left;">web</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Webcams &amp; Presence</td>
<td style="text-align: left;">Apache + Custom Perl</td>
<td style="text-align: left;">web</td>
<td style="text-align: left;"><a href="/user/atrophy">atrophy</a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">SpaceAPI</td>
<td style="text-align: left;">Apache + TBD Custom Code</td>
<td style="text-align: left;">web</td>
<td style="text-align: left;"><a href="/user/atrophy">atrophy</a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Databases</td>
<td style="text-align: left;">MySQL</td>
<td style="text-align: left;">db</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">CitrusDB</td>
<td style="text-align: left;">Apache + MySQL + More</td>
<td style="text-align: left;">citrus</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;">Mailing Lists</td>
<td style="text-align: left;">Mailman</td>
<td style="text-align: left;">lists</td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;">Fileserver</td>
<td style="text-align: left;">Samba, AFPd, NFS etc</td>
<td style="text-align: left;">fileserve</td>
<td style="text-align: left;"></td>
<td style="text-align: left;">Intended to be decommissioned in favor of dedicated NAS.</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Device AAA</td>
<td style="text-align: left;">Custom</td>
<td style="text-align: left;">access</td>
<td style="text-align: left;"><a href="/user/atrophy">atrophy</a><br />
<a href="/user/bdowning">bdowning</a></td>
<td style="text-align: left;">Intended to serve access lists etc to remote devices (eg: Door RFID controller).</td>
</tr>
</tbody>
</table>
