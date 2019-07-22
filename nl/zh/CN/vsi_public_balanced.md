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

# 均衡
{: #balanced}

均衡概要文件（使用网络连接存储器）能避免资源需求过量，因而可提高性能。网络性能的范围从标准到高级。

此产品通过以下概要文件来提供：

<table>
<CAPTION>表 1. 使用网络连接存储器的均衡概要文件</CAPTION>
<THEAD>
<TR>
<th>概要文件</th>
<th>vCPU</th>
<th>RAM</th>
<th>存储器类型</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>B1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>B1.48x192</td>
<td>48</td>
<td>192 GB</td>
<td>SAN</td>
</tr>
</TBODY>
</table>

**存储器说明**：

* SAN 主引导磁盘（25 GB 或 100 GB），有额外磁盘可用，每个磁盘最高 2 TB（总共允许 5 个磁盘）。
* 使用 SAN 存储器的公共虚拟服务器的定价包括虚拟 CPU、内存和最小主引导磁盘。额外磁盘价格取决于选择的磁盘大小和数量。  

均衡概要文件（使用网络连接存储器）在所有数据中心内均可用。

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。  
