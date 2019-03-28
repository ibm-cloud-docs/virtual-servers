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

# 内存
{: #memory}

内存概要文件最适合内存密集型工作负载，例如大型高速缓存工作负载、密集型数据库应用程序或内存中分析工作负载。

此产品通过以下概要文件来提供：

<table>
<CAPTION>表 1. 内存概要文件</CAPTION>
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
<td>M1.1x8</td>
<td>1</td>
<td>8 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.2x16</td>
<td>2</td>
<td>16 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.4x32</td>
<td>4</td>
<td>32 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.8x64</td>
<td>8</td>
<td>64 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.16x128</td>
<td>16</td>
<td>128 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.30x240</td>
<td>30</td>
<td>240 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.48x384</td>
<td>48</td>
<td>384 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.56x448</td>
<td>56</td>
<td>448 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>M1.64x512</td>
<td>64</td>
<td>512 GB</td>
<td>SAN</td>
</tr>
</TBODY>
</table>

**存储器说明**：
* SAN 主引导磁盘（25 GB 或 100 GB），有附加磁盘可用，每个磁盘最高 2 TB（总共允许 5 个磁盘）。
* 使用 SAN 存储器的公共虚拟服务器的定价包括虚拟 CPU、内存和最小主引导磁盘。附加磁盘价格取决于选择的磁盘大小和数量。  

内存概要文件在所有数据中心内均可用。

所有支持的操作系统（例如，RHEL、CentOS、Windows、Ubuntu 和其他操作系统）、支持的数据库以及软件附加组件也都可用于此产品。  
