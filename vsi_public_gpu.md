---



copyright:
  years: 2017, 2018
lastupdated: "2018-5-30"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU flavors are best for high performance workloads that require more compute density to reduce resource management and costs. The GPU flavors are ideal for intense graphic and data applications, or developing new applications that require fast performance.

Powered by NVDIA Tesla P100 GPUs, {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” flavor offers both block and local SSD storage. The following GPU flavors are available for you to choose from:  

  <table>
<CAPTION>Table 1. GPU flavors</CAPTION>
<THEAD>
<TR>
<th>Flavor</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>Storage Type</th>
<th>Boot Disc (GB)</th>
<th>Secondary Disc (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Block (SAN)</td>
<td>25 and 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Local SSD</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Block (SAN)</td>
<td>25 and 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Local SSD</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**Note:** GPU flavors are available in the _DAL13_ and _LON06_ datacenters.
<!--WDC07 end of May-->

## Before you begin
Review the following GPU prerequisites.

1. GPU flavor virtual servers are only available on an operating system that supports Hardware Virtual Machine (HVM) boot mode. See the following list for operating systems that HVM boot mode.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Appropriate NVIDIA drivers and software must be installed. For more information about software and NVIDIA drivers, see [Installing GPU drivers and software packages](../vsi/vsi_gpu_nvidia_drivers.html).  
**Note:** The software that you install might have prerequisite software and operating system-specific configurations.

# Add or remove GPUs
You can change the number of GPUs on your virtual server after your initial order. But, that depends on how many GPUs you provisioned. You have one of the following options. From the provisioning order screen, you have one of the following options
- If one GPU is provisioned, you can add another GPU, or
- If two GPUs are provisioned, you can fallback to one GPU
