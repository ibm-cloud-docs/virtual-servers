---



copyright:
  years: 2017, 2018
lastupdated: "2018-2-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU flavors are best for high performance workloads that require more compute density to reduce resource management and costs. GPUs are ideal for intense graphic and data applications, or developing new applications that require fast performance.

Powered by NVDIA Tesla P100 GPUs, {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” family offers both block (ac1) and local SSD storage (acl1). The following GPU flavors are available for you to choose from:  

<table>
<CAPTION>Table 1. GPU flavors</CAPTION>
<THEAD>
<TR>

<th></th>
<th>ac1.8x60</th>
<th>acl1.8x60</th>
<th>ac1.16x120</th>
<th>acl1.16x120</th>
</TR>
</THEAD>
<TBODY>
<tr>
<th scope="row">GPU</th>
<td>1 x P100</td>
<td>1 x P100</td>
<td>2 x P100</td>
<td>2 x P100</td>
</tr>
<tr>
<th scope="row">GPU RAM (GB)</th>
<td>16</td>
<td>16</td>
<td>32</td>
<td>32</td>
</tr>

<tr>
<th scope="row">vCPU</th>
<td>8</td>
<td>8</td>
<td>16</td>
<td>16</td>
</tr>

<tr>
<th scope="row">vCPU RAM (GB)</th>
<td>60</td>
<td>60</td>
<td>120</td>
<td>120</td>
</tr>

<tr>
<th scope="row">Storage Type</th>
<td>Block (SAN)</td>
<td>Local SSD</td>
<td>Block (SAN)</td>
<td>Local SSD</td>
</tr>

<tr>
<th scope="row">Boot Disc (GB)</th>
<td>25 and 100</td>
<td>100</td>
<td>25 and 100</td>
<td>100</td>
</tr>

<tr>
<th scope="row">Secondary Disc (GB)</th>
<td>4 x 2000</td>
<td>2 x 300</td>
<td>4 x 2000</td>
<td>2 x 300</td>
</tr>

</TBODY>
</table>


**Note:** GPU flavors are available in the _DAL13_ datacenter.

## Before you begin
Review the following GPU prerequisites.

1. GPU Family virtual servers are only available on an operating system that supports Hardware Virtual Machine (HVM) boot mode. See the following list for operating systems that HVM boot mode.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. Appropriate NVIDIA drivers and software must be installed. For more information about software and NVIDIA drivers, see [Installing GPU drivers and software packages](../vsi/vsi_gpu_nvidia_drivers.html).

**Note:** The software that you install might have prerequisite software and operating system-specific configurations.


