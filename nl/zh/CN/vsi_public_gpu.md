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
GPU 类型模板最适合需要更高计算密度以减少资源管理和成本的高性能工作负载。GPU 类型模板非常适合人工智能过程、密集的图形和数据应用程序，或者适合开发需要快速性能的新应用程序。

{{site.data.keyword.cloud_notm}} 加速计算“ac1”和“ac2”类型模板基于 NVDIA Tesla GPU 技术，同时提供块存储器和本地 SSD 存储器。以下 GPU 类型模板可供您选择：  

  <table>
<CAPTION>表 1. P100 GPU 类型模板</CAPTION>
<THEAD>
<TR>
<th>类型模板</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>存储器类型</th>
<th>引导盘 (GB)</th>
<th>辅助盘（2 个或 3 个）(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>块 (SAN)</td>
<td>25</td>
<td>无</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>本地 SSD 或 SAN</td>
<td>100</td>
<td>无 (SAN)<br>300（本地）</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>块 (SAN)</td>
<td>25</td>
<td>无</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>本地 SSD 或 SAN</td>
<td>100</td>
<td>无 (SAN)<br>600（本地）</td></tr>

</TBODY>
</table>

**注：**P100 GPU 类型模板在 _DAL13_、_LON06_ 和 _WDC07_ 数据中心内可用。

<table>
<CAPTION>表 2. V100 GPU 类型模板</CAPTION>
<THEAD>
<TR>
<th>类型模板</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>存储器类型</th>
<th>引导盘 (GB)</th>
<th>辅助盘（2 个或 3 个）(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 个 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>块 (SAN)</td>
<td>25</td>
<td>无</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 个 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>本地 SSD 或 SAN</td>
<td>100</td>
<td>无 (SAN)<br>300（本地）</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 个 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>块 (SAN)</td>
<td>25</td>
<td>无</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 个 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>本地 SSD 或 SAN</td>
<td>100</td>
<td>无 (SAN)<br>600（本地）</td></tr>

</TBODY>
</table>

**注：**V100 GPU 类型模板在 _DAL10_、_DAL12_ 和 _LON04_<!--WDC07--> 数据中心内可用。


## 开始之前
复查以下 GPU 先决条件。

1. GPU 类型模板虚拟服务器仅在支持硬件虚拟机 (HVM) 引导方式的操作系统上可用。有关支持 HVM 引导方式的操作系统，请参阅以下列表。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 必须安装相应的 NVIDIA 驱动程序和软件。有关软件和 NVIDIA 驱动程序的更多信息，请参阅[安装 GPU 驱动程序和软件包](../vsi/vsi_gpu_nvidia_drivers.html)。  
**注：**您安装的软件可能具有必备软件和特定于操作系统的配置。

## 添加或除去 GPU 
您可以在初始订购之后更改虚拟服务器上 GPU 的数量。但是，这取决于您供应的 GPU 的数量。您可以从以下选项中选择一个选项。

- 如果供应了一个 GPU，您可以再添加一个 GPU，或者
- 如果供应了两个 GPU，您可以回退到一个 GPU
