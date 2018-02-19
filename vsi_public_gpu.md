---



copyright:
  years: 2017, 2018
lastupdated: "2018-2-16"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU flavors are best for high performance workloads that require more compute density to reduce resource management and costs. GPUs are ideal for intense graphic and data applications, or developing new applications that require fast performance.

Powered by NVDIA Tesla P100 GPUs, {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” family offers both block and local SSD storage. The following GPU flavors are available for you to choose from:  

<CAPTION>Table 1. GPU flavors</CAPTION>
 
|| ac1.8x60 | acl1.8x60 | ac1.16x120 | acl1.16x120 |
|--| 
| <b>GPU</b> | 1 P100 | 1 P100 | 2 P100 | 2 P100 |
| <b>GPU RAM (GB)</b> | 16 | 16 | 32 | 32 |
| <b>vCPU</b> | 8 | 8 | 16 | 16|
| <b>vCPU RAM (GB)</b> | 60 | 60 | 120 | 120 |
| <b>Storage Type</b> | Block (SAN) | Local SSD | Block (SAN) | Local SSD |
| <b>Boot Disc (GB)</b> | 25 and 100 | 100 | 25 and 100 | 100 |
| <b>Secondary Disc (GB)</b> | 4 x 2000 | 2 x 300 | 4 x 2000 | 2 x 600 |

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


