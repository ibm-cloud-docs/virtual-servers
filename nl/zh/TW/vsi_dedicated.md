---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 專用虛擬伺服器
{{site.data.keyword.Bluemix}} 基礎架構專用主機供應項目是一部虛擬化的單一承租戶專用伺服器。它可讓您以最大限度控制工作負載放置及彈性後置佈建選項。您可以決定放入虛擬伺服器的預定 {{site.data.keyword.cloud}} 資料中心，以及將主機直接配置至帳戶來確保容量。
{:shortdesc}

此供應項目包括下列特性： 

* 親緣性及反親緣性。您可以指定應該保留的主機對虛擬伺服器以及虛擬伺服器對虛擬伺服器關係，稱為親緣性及反親緣性規則。這些規則可協助您根據工作負載需求來確定適當地放置工作負載。
* 後置部署管理。您可以根據工作負載需求，在專用主機之間移轉虛擬伺服器。
* 工作負載可見性。您可以檢視每一個主機的資源耗用量（核心、RAM 及本端儲存空間），讓您以最大限度控制工作負載管理。

您可以選擇兩種部署模型：專用主機及專用實例。專用主機有助於控制工作負載放置，而專用實例則提供單一承租戶隔離。 

**附註：**專用實例未提供專用主機所提供的一些控制特性。如需詳細資料，請參閱下表。 
<table>
<CAPTION>表 1. 控制特性</CAPTION>
<THEAD>
<TR>
<th>專用虛擬伺服器特性</th>
<th>專用主機實例</th>
<th>專用實例</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>單一承租戶隔離</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td>虛擬伺服器放置控制</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>資源可見性</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>實例計費</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td>主機計費<sup>(1)</sup></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>後置部署控制</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>容量保留</td>
<td>X</td>
<td></td>
</tr>
</TBODY>
</table>


<sup>(1)</sup>主機的定價包括核心、RAM、本端 SSD 及網路速度。將會使用每小時或每月模型中的現有定價及授權，針對每個實例的高階作業系統 (OS)、儲存區域網路 (SAN) 儲存空間及軟體附加程式進行收費。

當您要訂購專用主機及專用主機實例時，請記住下列項目：

* 您的主機位置；您可以從下列 {{site.data.keyword.cloud_notm}} 資料中心進行選取：
      
| 資料中心              ||
| ------------ | ------- | 
|AMS01         |  MON01  |
|AMS03         |  OSL01  |
|CHE01         |  PAR01  |
|DAL05         |  SAO01  |
|DAL06         |  SEO01  |
|DAL09         |  SJC01  |
|DAL10         |  SJC03  |
|DAL12         |  SJC04  |
|DAL13         |  SNG01  | 
|FRA02         |  SYD01  |
|HKG02         |  SYD04  |
|HOU02         |  TOK02  |
|LON02         |  TOR01  |
|LON04         |  WDC01  |
|MEL01         |  WDC04  |
|MEX01         |  WDC06  |
|MIL01         |  WDC07  |
{: caption="表 2. 支援的資料中心" caption-side="top"}

* 主機大小是根據您要在其上執行的工作負載所決定。預設值是 56 個核心 X 242 GB RAM X 1.2 TB。 
* 一次只能訂購兩個主機。例如，如果您需要六個主機，則仍然需要下三個不同的訂單。
* 每一個主機都需要自己的唯一名稱，而且您可以自動指派 POD。

## 後續步驟

在您檢閱及決定部署選項之後，即可佈建虛擬伺服器。若要開始使用，請參閱[佈建專用主機及實例](../vsi/vsi_provision_dedicated.html)。



  
