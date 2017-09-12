---



copyright:
  years: 2017
lastupdated: "2017-09-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Balanced local storage
The balanced local storage flavors are primarily for large database clusters that require high or low latency I/O performance. This offering has higher performance since the resources are not oversubscribed. Network performance ranges from standard to premium.

The offering is available in the following flavors:

<table>
<CAPTION>Table 1. Balanced local storage flavors</CAPTION>
<THEAD>
<TR>
<th>Flavor</th>
<th>Cores</th>
<th>Memory (GB)</th>
<th>Secondary storage (GB)<sup>(*)</sup></th>
<th>Storage type</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>Balanced Local-1</td>
<td>1</td>
<td>2</td>
<td>25, 100</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-2</td>
<td>1</td>
<td>4</td>
<td>25, 100</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-3</td>
<td>2</td>
<td>4</td>
<td>100, 200</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-4</td>
<td>2</td>
<td>8</td>
<td>100, 200</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-5</td>
<td>4</td>
<td>8</td>
<td>150, 300</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-6</td>
<td>4</td>
<td>16</td>
<td>150, 300</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-7</td>
<td>8</td>
<td>16</td>
<td>250, (2 x 250)</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-8</td>
<td>8</td>
<td>32</td>
<td>250, (2 x 250)</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-9</td>
<td>16</td>
<td>32</td>
<td>300, (2 x 300)</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-10</td>
<td>16</td>
<td>64</td>
<td>300, (2 x 300)</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-11</td>
<td>32</td>
<td>64</td>
<td>400, (2 x 400)</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-12</td>
<td>32</td>
<td>128</td>
<td>400, (2 x 400)</td>
<td>Local SSD, Local HDD</td>
</tr>
<tr>
<td>Balanced Local-13</td>
<td>56</td>
<td>242</td>
<td>2 x 750</td>
<td>Local SSD, Local HDD</td>
</tr>
</TBODY>
</table>

**Storage Notes:**
* <sup>(*)</sup>Balanced local flavors automatically come with a 100 GB local storage boot disk. Then, you must select a required, second disk (options shown in table above). Any additional local disks are optional. If you require over 500 GB, then two additional disks are required (for example, 8 cores require 2 x 250 GB of local storage).
*	Maximum local storage is limited by cores. 
*	Type of storage depends on data center location.
*	You cannot detach primary or secondary disks.


The following data centers support Balanced Local Storage virtual servers:

|Data Centers |        |
|------------ |------  |  
|AMS01        |HOU02   |
|DAL01        |SJC01   | 
|DAL05        |SJC04   |
|DAL06        |SEA01   |
|DAL13        |SNG01   |        
|HKG02        |WDC01   | 
{: caption="Table 2. Supported data centers" caption-side="top"}

All supported operating systems (such as RHEL, CentOS, Windows, Ubuntu, and others), supported  databases, and software add-ons are also available with this offering.  
