---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Balanced local storage
The balanced local storage profiles are primarily for large database clusters that require high or low latency I/O performance. This offering has higher performance since the resources are not oversubscribed. Network performance ranges from standard to premium.

The offering is available in various profiles and data centers, with the following local storage options:

* [Local HDD](/do/docs/vsi/vsi_public_balanced_local.html#HDD)
* [Local SSD](/do/docs/vsi/vsi_public_balanced_local.html#SSD)

## Local HDD {: #HDD}

<table>
<CAPTION>Table 1. Balanced local storage profiles using local HDD</CAPTION>
<THEAD>
<TR>
<th>Profile</th>
<th>vCPU</th>
<th>RAM</th>
<th>Secondary disks<sup>(*)</sup></th>
<th>Storage type</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Local HDD</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Local HDD</td>
</tr>
</TBODY>
</table>

**Storage Notes:**
* <sup>(*)</sup>Balanced local profiles automatically come with a 100 GB local storage boot disk. Then, you can select a second disk (options shown in table above). Any additional local disks are optional. If you require over 500 GB, then two additional disks are required (for example, 8 cores require 2 x 250 GB of local storage).
*	Maximum local storage is limited by cores.
*	Balanced local storage is globally available; however, the type of storage (Local SSD or Local HDD) depends on the data center location.
*	You cannot detach primary or secondary disks.

The following data centers support Balanced Local Storage virtual servers with local HDD:

|Data Centers (Local HDD) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   |
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="Table 1. Supported data centers (Local HDD)" caption-side="top"}

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), supported  databases, and software add-ons are also available with this offering.  

## Local SSD {: #SSD}
<table>
<CAPTION>Table 1. Balanced local storage profiles using local SSD</CAPTION>
<THEAD>
<TR>
<th>Profile</th>
<th>vCPU</th>
<th>RAM</th>
<th>Secondary disks<sup>(*)</sup></th>
<th>Storage type</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Local SSD</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Local SSD</td>
</tr>
</TBODY>
</table>

**Storage Notes:**
* <sup>(*)</sup>Balanced local profiles automatically come with a 100 GB local storage boot disk. Then, you can select a second disk (options shown in table above). Any additional local disks are optional. If you require over 500 GB, then two additional disks are required (for example, 8 cores require 2 x 250 GB of local storage).
*	Maximum local storage is limited by cores.
*	Balanced local storage is globally available; however, the type of storage (Local SSD or Local HDD) depends on the data center location.
*	You cannot detach primary or secondary disks.

The following data centers support Balanced Local Storage virtual servers with local SSD:

|Data Centers (Local SSD) |        |         |
|------- |------  |------ |
|AMS03   |LON06   |SJC03  |
|CHE01   |MEL01   |SJC04  |
|DAL09   |MEX01   |SYD01  |
|DAL10   |MIL01   |SYD04  |
|DAL12   |MON01   |TOK02  |       
|DAL13   |OSL01   |TOR01  |
|FRA02   |PAR01   |WDC04  |
|LON02   |SAO01   |WDC06  |
|LON04   |SEO01   | WDC07 |
{: caption="Table 2. Supported data centers (Local SSD)" caption-side="top"}

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), supported  databases, and software add-ons are also available with this offering.  
