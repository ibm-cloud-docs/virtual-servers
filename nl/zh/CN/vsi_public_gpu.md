---



copyright:
  years: 2017, 2018
lastupdated: "2018-2-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU 类型模板最适合需要更高计算密度以减少资源管理和成本的高性能工作负载。GPU 非常适合密集的图形和数据应用程序，或用于开发需要快速性能的新应用程序。

{{site.data.keyword.cloud_notm}} 加速计算“ac1”系列基于 NVDIA Tesla P100 GPU 技术，同时提供块 (ac1) 和本地 SSD 存储器 (acl1)。以下 GPU 类型模板可供您选择：  

<table>

<caption>表 1. GPU 类型模板</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">GPU 类型模板</th>
<tr>
  <th>ac1.8x60</th>
  <th>acl1.8x60</th>
  <th>ac1.16x120</th>
  <th>acl1.16x120</th>
</tr>
</thead>
<TBODY>
<tr>
  <th><b>GPU</b></th>
  <td>1 x P100</td>
  <td>1 x P100</td>
  <td>2 x P100</td>
  <td>2 x P100</td>
</tr>
<tr>
  <th><b>GPU RAM (GB)</b></th>
  <td>16</td>
  <td>16</td>
  <td>32</td>
  <td>32</td>
</tr>

<tr>
  <th><b>vCPU</b></th>
  <td>8</td>
  <td>8</td>
  <td>16</td>
  <td>16</td>
</tr>

<tr>
  <th><b>vCPU RAM (GB)</b></th>
  <td>60</td>
  <td>60</td>
  <td>120</td>
  <td>120</td>
</tr>

<tr>
  <th><b>存储器类型</b></th>
  <td>块 (SAN)</td>
  <td>本地 SSD</td>
  <td>块 (SAN)</td>
  <td>本地 SSD</td>
</tr>

<tr>
  <th><b>引导盘 (GB)</b></th>
  <td>25 和 100</td>
  <td>100</td>
  <td>25 和 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>辅助盘 (GB)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**注：**GPU 类型模板在 _DAL13_ 数据中心可用。

## 开始之前
复查以下 GPU 先决条件。

1. GPU 系列虚拟服务器仅在支持硬件虚拟机 (HVM) 引导方式的操作系统上可用。有关支持 HVM 引导方式的操作系统，请参阅以下列表。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. 必须安装相应的 NVIDIA 驱动程序和软件。有关软件和 NVIDIA 驱动程序的更多信息，请参阅[安装 GPU 驱动程序和软件包](../vsi/vsi_gpu_nvidia_drivers.html)。

**注：**您安装的软件可能具有必备软件和特定于操作系统的配置。


