---



copyright:
  years: 2017
lastupdated: "2017-11-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 平衡本端儲存空間
平衡本端儲存空間特性主要用於需要高或低延遲 I/O 效能的大型資料庫叢集。此供應項目具有較高效能，因為未超額訂閱資源。網路效能的範圍是從標準到高階。

供應項目可在各種特性及資料中心取得，並提供下列本端儲存選項：

* [本端 HDD](vsi_public_balanced_local.html#HDD)
* [本端 SSD](vsi_public_balanced_local.html#SSD)

## 本端 HDD {: #HDD}
 
<table>
<CAPTION>表 1. 使用本端 HDD 的平衡本端儲存空間特性</CAPTION>
<THEAD>
<TR>
<th>特性</th>
<th>vCPU</th>
<th>RAM</th>
<th>次要磁碟<sup>(*)</sup></th>
<th>儲存空間類型</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25、100 GB</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25、100 GB</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100、200 GB</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100、200 GB</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150、300 GB</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150、300 GB</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>本端 HDD </td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>本端 HDD </td>
</tr>
</TBODY>
</table>

**儲存空間附註：**
* <sup>(*)</sup>平衡本端特性自動隨附 100 GB 本端儲存空間開機磁碟。接著，您可以選取第二個磁碟（上表所顯示的選項）。任何其他本端磁碟都是選用的。如果您需要超過 500 GB，則需要兩個其他磁碟（例如，8 個核心需要 2 x 250 GB 的本端儲存空間）。
*	本端儲存空間上限受限於核心。 
*	平衡本端儲存空間可以在全球使用；不過，儲存空間的類型（本端 SSD 或本端 HDD）視資料中心位置而定。 
*	您無法分離主要或次要磁碟。

下列資料中心支援具有本端 HDD 的「平衡本端儲存空間」虛擬伺服器：

|資料中心（本端 HDD）|        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   | 
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02   |        |  
{: caption="表 1. 支援的資料中心（本端 HDD）" caption-side="top"}

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。  

## 本端 SSD {: #SSD}
<table>
<CAPTION>表 1. 使用本端 SSD 的平衡本端儲存空間特性</CAPTION>
<THEAD>
<TR>
<th>特性</th>
<th>vCPU</th>
<th>RAM</th>
<th>次要磁碟<sup>(*)</sup></th>
<th>儲存空間類型</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25、100 GB</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25、100 GB</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100、200 GB</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100、200 GB</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150、300 GB</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150、300 GB</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>本端 SSD </td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>本端 SSD </td>
</tr>
</TBODY>
</table>

**儲存空間附註：**
* <sup>(*)</sup>平衡本端特性自動隨附 100 GB 本端儲存空間開機磁碟。接著，您可以選取第二個磁碟（上表所顯示的選項）。任何其他本端磁碟都是選用的。如果您需要超過 500 GB，則需要兩個其他磁碟（例如，8 個核心需要 2 x 250 GB 的本端儲存空間）。
*	本端儲存空間上限受限於核心。 
*	平衡本端儲存空間可以在全球使用；不過，儲存空間的類型（本端 SSD 或本端 HDD）視資料中心位置而定。 
*	您無法分離主要或次要磁碟。

下列資料中心支援具有本端 SSD 的「平衡本端儲存空間」虛擬伺服器：

|資料中心（本端 SSD）|        |         |
|------- |------  |------ | 
|AMS03         |LON06   |SJC03  |
|CHE01         |MEL01         |SJC04  | 
|DAL09         |MEX01         |SYD01  |
|DAL10         |MIL01         |SYD04  |
|DAL12         |MON01  |TOK02  |       
|DAL13        |OSL01  |TOR01  |
|FRA02         |PAR01  |WDC04  |
|LON02         |SAO01  |WDC06  |
|LON04         |SEO01  | WDC07  | 
{: caption="表 2. 支援的資料中心（本端 SSD）" caption-side="top"}

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。  
