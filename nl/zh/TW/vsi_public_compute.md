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

# 計算
{: #compute}

計算設定檔最適合具有密集 CPU 需求的工作負載（例如高 Web 資料流量工作負載、正式作業批次處理及前端 Web 伺服器）。

下列設定檔可以使用此供應項目：

<table>
<CAPTION>表 1. 運算設定檔</CAPTION>
<THEAD>
<TR>
<th>設定檔</th>
<th>vCPU</th>
<th>RAM</th>
<th>儲存空間類型</th>
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

**儲存空間附註：**
* 有其他磁碟可用的 SAN 主要開機磁碟（25 或 100 GB），最高達每個 2 TB（共可允許 5 個磁碟）。
* 使用 SAN 儲存空間的公用虛擬伺服器的定價包括虛擬 CPU、記憶體及最小主要開機磁碟。其他磁碟價格取決於您選取的磁碟大小及數量。  

所有資料中心都提供運算設定檔。

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。  
