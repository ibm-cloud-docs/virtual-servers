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

# 计算
{: #compute}

计算概要文件最适合具有密集 CPU 需求的工作负载，例如高 Web 流量工作负载、生产批量处理和前端 Web 服务器。

此产品通过以下概要文件来提供：

<table>
<CAPTION>表 1. 计算概要文件</CAPTION>
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
<td>C1.1x1</td>
<td>1</td>
<td>1 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.2x2</td>
<td>2</td>
<td>2 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.4x4</td>
<td>4</td>
<td>4 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.8x8</td>
<td>8</td>
<td>8 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.16x16</td>
<td>16</td>
<td>16 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.32x32</td>
<td>32</td>
<td>32 GB</td>
<td>SAN</td>
</tr>
</TBODY>
</table>

**存储器说明**：
* SAN 主引导磁盘（25 GB 或 100 GB），有附加磁盘可用，每个磁盘最高 2 TB（总共允许 5 个磁盘）。
* 使用 SAN 存储器的公共虚拟服务器的定价包括虚拟 CPU、内存和最小主引导磁盘。附加磁盘价格取决于选择的磁盘大小和数量。  

计算概要文件在所有数据中心内均可用。

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。  
