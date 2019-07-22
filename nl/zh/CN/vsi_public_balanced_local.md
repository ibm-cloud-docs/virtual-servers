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

# 均衡本地存储器
{: #balanced-local-storage}

均衡本地存储器概要文件主要用于需要高流量、低延迟 I/O 性能的大型数据库集群。由于资源不会需求过量，所以此产品具有更高的性能。网络性能的范围从标准到高级。

此产品通过各种概要文件和数据中心来提供，具有以下本地存储器选项：

* [本地 HDD](/docs/vsi?topic=virtual-servers-HDD#HDD)
* [本地 SSD](/docs/vsi?topic=virtual-servers-SSD#SSD)

## 本地 HDD {: #HDD}

<table>
<CAPTION>表 1. 使用本地 HDD 的均衡本地存储器概要文件</CAPTION>
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

**存储器说明**：
* <sup>(*)</sup>均衡本地概要文件会自动随附 100 GB 的本地存储器引导磁盘。然后，可以选择第二个磁盘（选项见上表）。任何附加本地磁盘都是可选的。如果需要超过 500 GB 的磁盘，那么需要两个额外磁盘（例如，8 个核心需要 2 个 250 GB 的本地存储器）。
*	最大本地存储器受核心数的限制。
*	均衡本地存储器可供全局使用；但是，存储器的类型（本地 SSD 或本地 HDD）取决于数据中心的位置。
*	不能拆离主磁盘或辅助磁盘。

以下数据中心支持具有本地 HDD 的均衡本地存储器虚拟服务器：

|数据中心（本地 HDD）  |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   |
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02   |        |  
{: caption="表 1. 支持的数据中心（本地 HDD）" caption-side="top"}

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。  

## 本地 SSD {: #SSD}
<table>
<CAPTION>表 1. 使用本地 SSD 的均衡本地存储器概要文件</CAPTION>
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

**存储器说明**：
* <sup>(*)</sup>均衡本地概要文件会自动随附 100 GB 的本地存储器引导磁盘。然后，可以选择第二个磁盘（选项见上表）。任何附加本地磁盘都是可选的。如果需要超过 500 GB 的磁盘，那么需要两个额外磁盘（例如，8 个核心需要 2 个 250 GB 的本地存储器）。
*	最大本地存储器受核心数的限制。
*	均衡本地存储器可供全局使用；但是，存储器的类型（本地 SSD 或本地 HDD）取决于数据中心的位置。
*	不能拆离主磁盘或辅助磁盘。

以下数据中心支持具有本地 SSD 的均衡本地存储器虚拟服务器：

|数据中心（本地 SSD）     |        |         |
|------- |------  |------ |
|AMS03         |LON06   |SJC03  |
|CHE01         |MEL01         |SJC04  |
|DAL09         |MEX01         |SYD01  |
|DAL10         |MIL01         |SYD04  |
|DAL12         |MON01  |TOK02  |       
|DAL13        |OSL01  |TOR01  |
|FRA02         |PAR01  |WDC04  |
|LON02         |SAO01  |WDC06  |
|LON04         |SEO01  |WDC07  |
{: caption="表 2. 支持的数据中心（本地 SSD）" caption-side="top"}

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。  
