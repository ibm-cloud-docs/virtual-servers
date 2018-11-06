---



copyright:
  years: 2017, 2018
lastupdated: "2018-09-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU flavors are best for high-performance workloads that require more compute density to reduce resource management and costs. The GPU flavors are ideal for artificial intelligence processes, intense graphic and data applications, or developing new applications that require fast performance.

Powered by NVDIA Tesla GPUs, {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” and "ac2" flavors both offer block and local SSD storage. The following GPU flavors are available for you to choose from:  

  <table>
<CAPTION>Table 1. P100 GPU flavors</CAPTION>
<THEAD>
<TR>
<th>Flavor</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>Storage Type</th>
<th>Boot Disc (GB)</th>
<th>Secondary Discs (2 and 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Block (SAN)</td>
<td>25</td>
<td>None</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Local SSD or SAN</td>
<td>100</td>
<td>None (SAN)<br>300 (Local)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Block (SAN)</td>
<td>25</td>
<td>None</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Local SSD or SAN</td>
<td>100</td>
<td>None (SAN)<br>600 (Local)</td></tr>

</TBODY>
</table>

**Note:** P100 GPU flavors are available in the _DAL13_, _LON06_, and _WDC07_ datacenters.

<table>
<CAPTION>Table 2. V100 GPU flavors</CAPTION>
<THEAD>
<TR>
<th>Flavor</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>Storage Type</th>
<th>Boot Disc (GB)</th>
<th>Secondary Discs (2 and 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Block (SAN)</td>
<td>25</td>
<td>None</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Local SSD or SAN</td>
<td>100</td>
<td>None (SAN)<br>300 (Local)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Block (SAN)</td>
<td>25</td>
<td>None</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Local SSD or SAN</td>
<td>100</td>
<td>None (SAN)<br>600 (Local)</td></tr>

</TBODY>
</table>

**Note:** V100 GPU flavors are available in the _DAL10_, _DAL12_, and _LON04_, and WDC07 datacenters.


## Before you begin
Review the following GPU prerequisites.

1. GPU flavor virtual servers are only available on an operating system that supports Hardware Virtual Machine (HVM) boot mode. See the following list for operating systems that support HVM boot mode.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Appropriate NVIDIA drivers and software must be installed. For more information about software and NVIDIA drivers, see [Installing GPU drivers and software packages](../vsi/vsi_gpu_nvidia_drivers.html).  
**Note:** The software that you install might have prerequisite software and operating system-specific configurations.

## Add or remove GPUs 
You can change the number of GPUs on your virtual server after your initial order. But, that depends on how many GPUs you provisioned. You have one of the following options.

- If one GPU is provisioned, you can add another GPU, or
- If two GPUs are provisioned, you can fallback to one GPU
