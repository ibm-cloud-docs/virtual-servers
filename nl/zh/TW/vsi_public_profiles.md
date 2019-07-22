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

# 設定檔
{: #about-virtual-server-profiles}

當您佈建 {{site.data.keyword.cloud}} 虛擬伺服器實例時，可以從支援的設定檔系列中選取。設定檔是 vCPU 和 RAM 的組合，可以快速實例化以啟動虛擬伺服器實例。在 {{site.data.keyword.cloud_notm}} 主控台中，您可以從熱門的設定檔配置中選擇，或從最符合您需求的設定檔清單中選取。
{:shortdesc}

下列是可用的虛擬伺服器實例系列。

取決於您的實例類型，部分系列可能無法使用。
{:note}

| 系列  |說明                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[平衡](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) |最適合需要效能及可調整性平衡的一般雲端工作負載。使用網路連結的儲存空間。|
|[平衡本端儲存空間](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) |最適合需要高 I/O 效能且延遲很低的大型資料庫工作負載。|
|[計算](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) |最適合中到高 Web 資料流量工作負載。|
|[記憶體](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  |最適合記憶體快取及即時分析工作負載。
|
|[GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  |最適合高效能工作負載。
|
{: caption="表 1. 公用虛擬伺服器系列選項" caption-side="top"}

這些系列有部分也可用於 IBM Cloud Virtual Servers for VPC。如需相關資訊，請參閱 [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen)。
{:tip}

## 平衡
{: #balanced}

平衡設定檔（具有網路連結的儲存空間）很適合需要效能與規模平衡的一般雲端工作負載。網路效能的範圍是從標準到高階。

下列設定檔可以使用此供應項目：

| 設定檔                  |vCPU|RAM|儲存空間類型|
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
{: caption="表 2. 具有網路連結儲存空間的平衡設定檔" caption-side="top"}

### 儲存空間注意事項

* 有其他磁碟可用的 SAN 主要開機磁碟（25 或 100 GB），最高為每個磁碟 2 TB（共可容許五個磁碟）。
* 使用 SAN 儲存空間的公用虛擬伺服器的定價包括虛擬 CPU、記憶體及最小主要開機磁碟。額外磁碟價格取決於您選取的磁碟大小和數量。  

所有資料中心都提供平衡設定檔（含有網路連結的儲存空間）。

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。 

## 平衡本端儲存空間
{: #balanced-local-storage}

平衡本端儲存空間設定檔主要用於需要高 I/O 效能且延遲很低的大型資料庫工作負載。網路效能的範圍是從標準到高階。

供應項目可在各種設定檔及資料中心取得，並提供下列本端儲存選項：

* [本端 HDD ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [本端 SSD ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### 本端 HDD 
{: #HDD}
 
<table>
<CAPTION>表 3. 使用本端 HDD 的平衡本端儲存空間設定檔</CAPTION>
<THEAD>
<TR>
<th>設定檔</th>
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

#### 儲存空間注意事項
* <sup>(*)</sup>平衡本端設定檔自動配備 100 GB 本端儲存空間開機磁碟。接著，您可以選取第二個磁碟（表 3 中顯示的選項）。任何其他本端磁碟都是選用的。如果您需要超過 500 GB，則需要兩個其他磁碟（例如，8 個核心需要 2 x 250 GB 的本端儲存空間）。
*	本端儲存空間上限受限於核心。 
*	平衡本端儲存空間可以在全球使用；不過，儲存空間的類型（本端 SSD 或本端 HDD）視資料中心位置而定。 
*	您無法分離主要或次要磁碟。

下列資料中心支援具有本端 HDD 的平衡本端儲存空間虛擬伺服器：

|可用的資料中心 - 本端 HDD|       |
| ---------------------- | ----- |
|達拉斯 (DAL01)|達拉斯 (DAL05)|
|達拉斯 (DAL06)|休斯頓 (HOU02)|
|西雅圖 (SEA01)|聖荷西 (SJC01)|
|華盛頓特區 (WDC01)|                  |
{: class="simple-tab-table"}
{: caption="表 4. 可用的資料中心（本端 HDD）- 美洲" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

|可用的資料中心 - 本端 HDD|
| ---------------------- |
|阿姆斯特丹 (AMS01)|
{: class="simple-tab-table"}
{: caption="表 5. 可用的資料中心（本端 HDD）- 歐洲" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

|可用的資料中心 - 本端 HDD|
| ---------------------- |
|香港 (HKG02)| 
|新加坡 (SNG01)|
{: class="simple-tab-table"}
{: caption="表 6. 可用的資料中心（本端 HDD）- 亞太地區" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。  

### 本端 SSD  
{: #SSD}

<table>
<CAPTION>表 7. 使用本端 SSD 的平衡本端儲存空間設定檔</CAPTION>
<THEAD>
<TR>
<th>設定檔</th>
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

#### 儲存空間注意事項
* <sup>(*)</sup>平衡本端設定檔自動配備 100 GB 本端儲存空間開機磁碟。接著，您可以選取第二個磁碟（上表所顯示的選項）。任何其他本端磁碟都是選用的。如果您需要超過 500 GB，則需要兩個其他磁碟（例如，8 個核心需要 2 x 250 GB 的本端儲存空間）。
*	本端儲存空間上限受限於核心。 
*	平衡本端儲存空間可以在全球使用；不過，儲存空間的類型（本端 SSD 或本端 HDD）視資料中心位置而定。 
*	您無法分離主要或次要磁碟。

下列資料中心支援具有本端 SSD 的平衡本端儲存空間虛擬伺服器：

|可用的資料中心 - 本端 SDD|        |
| ---------------------------------- | ------ |
|達拉斯 (DAL09)|達拉斯 (DAL10)|
|達拉斯 (DAL12)|達拉斯 (DAL13)|
|克雷塔羅 (MEX01)|蒙特婁 (MON01)|
|聖保羅 (SAO01)|聖荷西 (SJC03)|
|聖荷西 (SJC04)|多倫多 (TOR01)|
|華盛頓特區 (WDC04)|華盛頓特區 (WDC06)|
|華盛頓特區 (WDC07)|                        |
{: class="simple-tab-table"}
{: caption="表 8. 可用的資料中心（本端 SDD）- 美洲" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

|可用的資料中心 - 本端 SDD|       |
| ---------------------------------- | ----- |
|阿姆斯特丹 (AMS03)|法蘭克福 (FRA02)|
|倫敦 (LON02)|倫敦 (LON04)|
|倫敦 (LON06)|米蘭 (MIL01)|
|奧斯陸 (OSL01)|巴黎 (PAR01)|
{: class="simple-tab-table"}
{: caption="表 9. 可用的資料中心（本端 SDD）- 歐洲" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

|可用的資料中心 - 本端 SDD|       |
| ---------------------------------- | ----- |
|清奈 (CHE01)|墨爾本 (MEL01)|
|首爾 (SEO01)|雪梨 (SYD01)|
|雪梨 (SYD04)|東京 (TOK02)|
{: class="simple-tab-table"}
{: caption="表 10. 可用的資料中心（本端 SDD）－亞太地區" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。

## 運算
{: #compute}

計算設定檔最適合具有密集 CPU 需求的工作負載（例如高 Web 資料流量工作負載、正式作業批次處理及前端 Web 伺服器）。

下列設定檔可以使用此供應項目：

| 設定檔                  |vCPU|RAM|儲存空間類型|
| ------------ | -------- | --------- | ------------ |
|C1.1x1|1|1 GB|SAN|
|C1.2x2|2|2 GB|SAN|
|C1.4x4|4|4 GB|SAN|
|C1.8x8|8|8 GB|SAN|
|C1.16x16|16|16 GB|SAN|
|C1.32x32|32|32 GB|SAN|
{: caption="表 11. 運算設定檔" caption-side="top"}

### 儲存空間注意事項
* 有其他磁碟可用的 SAN 主要開機磁碟（25 或 100 GB），最高為每個磁碟 2 TB（共可容許五個磁碟）。
* 使用 SAN 儲存空間的公用虛擬伺服器的定價包括虛擬 CPU、記憶體及最小主要開機磁碟。額外磁碟價格取決於您選取的磁碟大小和數量。  

所有資料中心都提供運算設定檔。

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。

## 記憶體
{: #memory}

記憶體設定檔最適合記憶體密集工作負載（例如大型快取工作負載、密集資料庫應用程式，或記憶體內分析工作負載）。

下列設定檔可以使用此供應項目：

| 設定檔                  |vCPU|RAM|儲存空間類型|
| ------------ | -------- | --------- | ------------ |
|M1.1x8|1|8 GB|SAN|
|M1.2x16|2|16 GB|SAN|
|M1.4x32|4|32 GB|SAN|
|M1.8x64|8|64 GB|SAN|
|M1.16x128|16|128 GB|SAN|
|M1.30x240|30|240 GB|SAN|
|M1.48x384|48|384 GB|SAN|
|M1.56x448|56 	|448 GB|SAN|
|M1.64x512|64|512 GB|SAN|
{: caption="表 12. 記憶體設定檔" caption-side="top"}

### 儲存空間注意事項
* 有其他磁碟可用的 SAN 主要開機磁碟（25 或 100 GB），最高達每個 2 TB（共可允許 5 個磁碟）。
* 使用 SAN 儲存空間的公用虛擬伺服器的定價包括虛擬 CPU、記憶體及最小主要開機磁碟。其他磁碟價格取決於您選取的磁碟大小及數量。  

所有資料中心都提供記憶體設定檔。

此供應項目也提供所有支援的作業系統（例如 RHEL、CentOS、Windows、Ubuntu 及其他）、支援的資料庫以及軟體附加程式。

## GPU
{: #gpu}

GPU 設定檔最適用於高效能工作負載，這些工作負載需要更高的運算密度才能減少資源管理及成本。GPU 設定檔完全適合人工智慧處理程序、大量圖形及資料的應用程式，或開發需要快速效能的新應用程式。

{{site.data.keyword.cloud_notm}} Accelerated Compute "ac1" 和 "ac2" 設定檔採用 NVDIA Tesla GPU 技術，且兩者都提供區塊和本端 SSD 儲存空間。您可以從中選擇下列 GPU 設定檔：  

<table>
<CAPTION>表 13. P100 GPU 設定檔</CAPTION>
<THEAD>
<TR>
<th>設定檔</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>儲存空間類型</th>
<th>開機磁碟 (GB)</th>
<th>次要磁碟（2 及 3）(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>300（本端）</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>600（本端）</td></tr>

</TBODY>
</table>

_DAL13_、_LON06_ 及 _WDC07_ 資料中心內提供 P100 GPU 設定檔。
{: note}

<table>
<CAPTION>表 14. V100 GPU 設定檔</CAPTION>
<THEAD>
<TR>
<th>設定檔</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>儲存空間類型</th>
<th>開機磁碟 (GB)</th>
<th>次要磁碟（2 及 3）(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>300（本端）</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>區塊 (SAN)</td>
<td>25</td>
<td>無</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>本端 SSD 或 SAN</td>
<td>100</td>
<td>無 (SAN)<br>600（本端）</td></tr>

</TBODY>
</table>

_DAL10_、_DAL12_、_LON04_ 及 _WDC07_ 資料中心內提供 V100 GPU 設定檔。
{: note}

### GPU 必要條件
請檢閱下列 GPU 必要條件。

1. 只有支援「硬體虛擬機器 (HVM)」開機模式的作業系統上才提供 GPU 設定檔虛擬伺服器。請參閱下列清單，以取得支援 HVM 開機模式的作業系統。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 必須安裝適當的 NVIDIA 驅動程式及軟體。如需軟體及 NVIDIA 驅動程式的相關資訊，請參閱[安裝 GPU 驅動程式及軟體套件](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages)。  

您安裝的軟體可能有必備軟體和作業系統特定配置。
{: note}

### 新增或移除 GPU 
您可以在起始訂購之後變更虛擬伺服器上的 GPU 數目。但是，這取決於您已佈建的 GPU 數目。您會有下列其中一個選項。

- 如果佈建一個 GPU，則您可以新增另一個 GPU，或者
- 如果佈建兩個 GPU，則您可以撤回至一個 GPU

