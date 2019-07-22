---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

keywords: public virtual servers, network traffic, virtual server deployment, profile

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 概要文件
{: #about-virtual-server-profiles}

当您供应 {{site.data.keyword.cloud}} 虚拟服务器实例时，可以从受支持的概要文件系列中进行选择。配置文件是 vCPU 和 RAM 的组合，可以快速实例化以启动虚拟服务器实例。在 {{site.data.keyword.cloud_notm}} 控制台中，您可以从常用的概要文件配置中进行选择，也可以从最适合您需要的概要文件列表中进行选择。
{:shortdesc}

提供了以下虚拟服务器实例系列。

根据您的实例类型，某些系列可能不可用。
{:note}

| 系列  |描述|
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[均衡](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced)|最适用于需要均衡性能和可扩展性的常用云工作负载。使用网络连接存储器。|
|[均衡本地存储器](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage)|最适用于需要等待时间极低的高 I/O 性能的大型数据库工作负载。|
|[计算](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute)|最适用于中到高 Web 流量工作负载。|
|[内存](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)|最适用于内存高速缓存和实时分析工作负载。
|
|[GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)|最适用于高性能工作负载。
|
{: caption="表 1. 公共虚拟服务器系列选择" caption-side="top"}

上述某些系列也可用于 IBM Cloud Virtual Server for VPC。有关更多信息，请参阅 [IBM Cloud Virtual Server for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen)。
{:tip}

## 均衡
{: #balanced}

均衡概要文件（具有网络连接存储器）非常适合用于需要均衡性能和规模的常用云工作负载。网络性能的范围从标准到高级。

此产品通过以下概要文件来提供：

|概要文件|vCPU|RAM|存储器类型|
| --------- | ------- | ------- | ------------ |
|B1.1x2|1|2 GB|SAN|
|B1.1x4|1|4 GB|SAN|
|B1.2x4|2|4 GB|SAN|
|B1.2x8|2|8 GB|SAN|
|B1.4x8|4|8 GB|SAN|
|B1.4x16|4|16 GB|SAN|
|B1.8x16|8|16 GB|SAN|
|B1.8x32|8|32 GB|SAN|
|B1.16x32|16|32 GB|SAN|
|B1.16x64|16|64 GB|SAN|
|B1.32x64|32|64 GB|SAN|
|B1.32x128|32|128 GB|SAN|
|B1.48x192|48|192 GB|SAN|
{: caption="表 2. 使用网络连接存储器的均衡概要文件" caption-side="top"}

### 存储器注释

* SAN 主引导磁盘（25 GB 或 100 GB），有额外磁盘可用，每个磁盘最高 2 TB（总共允许 5 个磁盘）。
* 使用 SAN 存储器的公共虚拟服务器的定价包括虚拟 CPU、内存和最小主引导磁盘。额外磁盘价格取决于选择的磁盘大小和数量。  

均衡概要文件（使用网络连接存储器）在所有数据中心内均可用。

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。 

## 均衡本地存储器
{: #balanced-local-storage}

均衡本地存储器概要文件主要适用于需要等待时间极低的高 I/O 性能的大型数据库工作负载。网络性能的范围从标准到高级。

此产品通过各种概要文件和数据中心来提供，具有以下本地存储器选项：

* [本地 HDD](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [本地 SSD](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### 本地 HDD
{: #HDD}
 
<table>
<CAPTION>表 3. 使用本地 HDD 的均衡本地存储器概要文件</CAPTION>
<THEAD>
<TR>
<th>概要文件</th>
<th>vCPU</th>
<th>RAM</th>
<th>辅助磁盘 <sup>(*)</sup></th>
<th>存储器类型</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25 GB，100 GB</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25 GB，100 GB</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100 GB，200 GB</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100 GB，200 GB</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150 GB，300 GB</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150 GB，300 GB</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB，(2 x 250 GB)</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB，(2 x 250 GB)</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB，(2 x 300 GB)</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB，(2 x 300 GB)</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB，(2 x 400 GB)</td>
<td>本地 HDD</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB，(2 x 400 GB)</td>
<td>本地 HDD</td>
</tr>
</TBODY>
</table>

#### 存储器注释
* <sup>(*)</sup>均衡本地概要文件会自动随附 100 GB 的本地存储器引导磁盘。然后，可以选择第二个磁盘（表 3 中所示的选项）。任何附加本地磁盘都是可选的。如果需要超过 500 GB 的磁盘，那么需要两个额外磁盘（例如，8 个核心需要 2 个 250 GB 的本地存储器）。
*	最大本地存储器受核心数的限制。 
*	均衡本地存储器可供全局使用；但是，存储器的类型（本地 SSD 或本地 HDD）取决于数据中心的位置。 
*	不能拆离主磁盘或辅助磁盘。

以下数据中心支持具有本地 HDD 的均衡本地存储器虚拟服务器：

| 可用数据中心 - 本地 HDD|       |
| ---------------------- | ----- |
| 达拉斯 (DAL01)         | 达拉斯 (DAL05)   |
| 达拉斯 (DAL06)         | 休斯顿 (HOU02)   |
| 西雅图 (SEA01)         | 圣何塞 (SJC01)   |
| 华盛顿特区 (WDC01) |                  |
{: class="simple-tab-table"}
{: caption="表 4. 可用数据中心（本地 HDD）- 美洲" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| 可用数据中心 - 本地 HDD|
| ---------------------- |
| 阿姆斯特丹 (AMS01)     |
{: class="simple-tab-table"}
{: caption="表 5. 可用数据中心（本地 HDD）- 欧洲" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| 可用数据中心 - 本地 HDD|
| ---------------------- |
| 中国香港特别行政区 (HKG02)| 
| 新加坡 (SNG01)      |
{: class="simple-tab-table"}
{: caption="表 6. 可用数据中心（本地 HDD）- 亚太地区" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。  

### 本地 SSD 
{: #SSD}

<table>
<CAPTION>表 7. 使用本地 SSD 的均衡本地存储器概要文件</CAPTION>
<THEAD>
<TR>
<th>概要文件</th>
<th>vCPU</th>
<th>RAM</th>
<th>辅助磁盘 <sup>(*)</sup></th>
<th>存储器类型</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25 GB，100 GB</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25 GB，100 GB</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100 GB，200 GB</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100 GB，200 GB</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150 GB，300 GB</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150 GB，300 GB</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB，(2 x 250 GB)</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB，(2 x 250 GB)</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB，(2 x 300 GB)</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB，(2 x 300 GB)</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB，(2 x 400 GB)</td>
<td>本地 SSD</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB，(2 x 400 GB)</td>
<td>本地 SSD</td>
</tr>
</TBODY>
</table>

#### 存储器注释
* <sup>(*)</sup>均衡本地概要文件会自动随附 100 GB 的本地存储器引导磁盘。然后，可以选择第二个磁盘（选项见上表）。任何附加本地磁盘都是可选的。如果需要超过 500 GB 的磁盘，那么需要两个额外磁盘（例如，8 个核心需要 2 个 250 GB 的本地存储器）。
*	最大本地存储器受核心数的限制。 
*	均衡本地存储器可供全局使用；但是，存储器的类型（本地 SSD 或本地 HDD）取决于数据中心的位置。 
*	不能拆离主磁盘或辅助磁盘。

以下数据中心支持具有本地 SSD 的均衡本地存储器虚拟服务器：

| 可用数据中心 - 本地 SDD|        |
| ---------------------------------- | ------ |
| 达拉斯 (DAL09)                     | 达拉斯 (DAL10)         |
| 达拉斯 (DAL12)                     | 达拉斯 (DAL13)         |
| 克雷塔罗 (MEX01)                   | 蒙特利尔 (MON01)       |
| 圣保罗 (SAO01)                     | 圣何塞 (SJC03)         |
| 圣何塞 (SJC04)                     | 多伦多 (TOR01)         |
| 华盛顿特区 (WDC04)                 | 华盛顿特区 (WDC06)     |
| 华盛顿特区 (WDC07)                 |                        |
{: class="simple-tab-table"}
{: caption="表 8. 可用数据中心（本地 SDD）- 美洲" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| 可用数据中心 - 本地 SDD|       |
| ---------------------------------- | ----- |
| 阿姆斯特丹 (AMS03)                 | 法兰克福 (FRA02)  |
| 伦敦 (LON02)                       | 伦敦 (LON04)      |
| 伦敦 (LON06)                       | 米兰 (MIL01)      |
| 奥斯陆 (OSL01)                     | 巴黎 (PAR01)      |
{: class="simple-tab-table"}
{: caption="表 9. 可用数据中心（本地 SDD）- 欧洲" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| 可用数据中心 - 本地 SDD|       |
| ---------------------------------- | ----- |
| 金奈 (CHE01)                       | 墨尔本 (MEL01)    |
| 首尔 (SEO01)                       | 悉尼 (SYD01)      |
| 悉尼 (SYD04)                       | 东京 (TOK02)      |
{: class="simple-tab-table"}
{: caption="表 10. 可用数据中心（本地 SDD）- 亚太地区" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。

## 计算
{: #compute}

计算概要文件最适合具有密集 CPU 需求的工作负载，例如高 Web 流量工作负载、生产批量处理和前端 Web 服务器。

此产品通过以下概要文件来提供：

|概要文件|vCPU|RAM|存储器类型|
| ------------ | -------- | --------- | ------------ |
|C1.1x1|1|1 GB|SAN|
|C1.2x2|2|2 GB|SAN|
|C1.4x4|4|4 GB|SAN|
|C1.8x8|8|8 GB|SAN|
|C1.16x16|16|16 GB|SAN|
|C1.32x32|32|32 GB|SAN|
{: caption="表 11. 计算概要文件" caption-side="top"}

### 存储器注释
* SAN 主引导磁盘（25 GB 或 100 GB），有额外磁盘可用，每个磁盘最高 2 TB（总共允许 5 个磁盘）。
* 使用 SAN 存储器的公共虚拟服务器的定价包括虚拟 CPU、内存和最小主引导磁盘。额外磁盘价格取决于选择的磁盘大小和数量。  

计算概要文件在所有数据中心内均可用。

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。

## 内存
{: #memory}

内存概要文件最适合内存密集型工作负载，例如大型高速缓存工作负载、密集型数据库应用程序或内存中分析工作负载。

此产品通过以下概要文件来提供：

|概要文件|vCPU|RAM|存储器类型|
| ------------ | -------- | --------- | ------------ |
|M1.1x8|1|8 GB|SAN|
|M1.2x16|2|16 GB|SAN|
|M1.4x32|4|32 GB|SAN|
|M1.8x64|8|64 GB|SAN|
|M1.16x128|16|128 GB|SAN|
|M1.30x240|30|240 GB|SAN|
|M1.48x384|48|384 GB|SAN|
|M1.56x448|56|448 GB|SAN|
|M1.64x512|64|512 GB|SAN|
{: caption="表 12. 内存概要文件" caption-side="top"}

### 存储器注释
* SAN 主引导磁盘（25 GB 或 100 GB），有额外磁盘可用，每个磁盘最高 2 TB（总共允许 5 个磁盘）。
* 使用 SAN 存储器的公共虚拟服务器的定价包括虚拟 CPU、内存和最小主引导磁盘。额外磁盘价格取决于选择的磁盘大小和数量。  

内存概要文件在所有数据中心内均可用。

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。

## GPU
{: #gpu}

GPU 概要文件最适合需要更高计算密度以减少资源管理和成本的高性能工作负载。GPU 概要文件非常适合人工智能过程、图形和数据密集型应用程序，也适合开发需要快速性能的新应用程序。

{{site.data.keyword.cloud_notm}} 加速计算“ac1”和“ac2”概要文件基于 NVDIA Tesla GPU 技术，同时提供块存储器和本地 SSD 存储器。以下 GPU 概要文件可供您选择：  

<table>
<CAPTION>表 13. P100 GPU 概要文件</CAPTION>
<THEAD>
<TR>
<th>概要文件</th>
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

P100 GPU 概要文件在 _DAL13_、_LON06_ 和 _WDC07_ 数据中心内可用。
{: note}

<table>
<CAPTION>表 14. V100 GPU 概要文件</CAPTION>
<THEAD>
<TR>
<th>概要文件</th>
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

V100 GPU 概要文件在 _DAL10_、_DAL12_、_LON04_ 和 _WDC07_ 数据中心内可用。
{: note}

### GPU 先决条件
复查以下 GPU 先决条件。

1. GPU 概要文件虚拟服务器仅在支持硬件虚拟机 (HVM) 引导方式的操作系统上可用。有关支持 HVM 引导方式的操作系统，请参阅以下列表。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 必须安装相应的 NVIDIA 驱动程序和软件。有关软件和 NVIDIA 驱动程序的更多信息，请参阅[安装 GPU 驱动程序和软件包](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages)。  

您安装的软件可能具有必备软件和特定于操作系统的配置。
{: note}

### 添加或除去 GPU 
您可以在初始订购之后更改虚拟服务器上 GPU 的数量。但是，这取决于您供应的 GPU 的数量。您可以从以下选项中选择一个选项。

- 如果供应了一个 GPU，您可以再添加一个 GPU，或者
- 如果供应了两个 GPU，您可以回退到一个 GPU

