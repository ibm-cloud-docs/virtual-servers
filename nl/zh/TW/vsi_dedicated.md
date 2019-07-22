---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# 關於專用虛擬伺服器
{: #dedicated-virtual-servers}

{{site.data.keyword.Bluemix}} 基礎架構專用主機供應項目是一部虛擬化的單一承租戶專用伺服器。它可讓您對於工作負載放置及彈性後置佈建選項有最大的控制權。您可以決定放入虛擬伺服器的預定 {{site.data.keyword.cloud_notm}} 資料中心，以及將主機直接配置至帳戶來確保容量。
{:shortdesc}

此供應項目包括下列特性：

* 親緣性及反親緣性。您可以指定應該保留的主機對虛擬伺服器以及虛擬伺服器對虛擬伺服器關係，稱為親緣性及反親緣性規則。這些規則可協助您根據工作負載需求來確定適當地放置工作負載。
* 後置部署管理。您可以根據工作負載需求，在專用主機之間移轉虛擬伺服器。
* 工作負載可見性。您可以檢視每一個主機的資源耗用量（核心、RAM 及本端儲存空間），讓您對工作負載管理有最大的控制權。

您可以選擇兩種部署模型：專用主機及專用實例。專用主機有助於控制工作負載放置，而專用實例則提供單一承租戶隔離。

專用實例未提供專用主機所提供的一些控制特性。如需詳細資料，請參閱下表。{:note}

|專用虛擬伺服器特性|專用主機實例|專用實例|
| ------- | ------- | ------- |
|單一承租戶隔離| ![勾號圖示](../../icons/checkmark-icon.svg) | ![勾號圖示](../../icons/checkmark-icon.svg) |
|虛擬伺服器放置控制| ![勾號圖示](../../icons/checkmark-icon.svg) |   |
|資源可見性| ![勾號圖示](../../icons/checkmark-icon.svg) |   |
|實例計費|   | ![勾號圖示](../../icons/checkmark-icon.svg) |
|主機計費<sup>(1)</sup> | ![勾號圖示](../../icons/checkmark-icon.svg) |   |
|後置部署控制| ![勾號圖示](../../icons/checkmark-icon.svg) |   |
|容量保留| ![勾號圖示](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="表 1. 控制特性" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>主機的定價包括核心、RAM、本端 SSD 及網路速度。將會使用每小時或每月模型中的現有定價及授權，針對每個實例的高階作業系統 (OS)、儲存區域網路 (SAN) 儲存空間及軟體附加程式進行收費。

當您要訂購專用主機及專用主機實例時，請記住下列項目：

* 主機大小是根據您要在其上執行的工作負載所決定。預設值是 56 核心 X 242 GB RAM X 1.2 TB，但您可以從其他配置中選擇。
* 一次只能訂購兩個主機。例如，如果您需要六個主機，則仍然需要下三個不同的訂單。
* 每一個主機都需要自己的唯一名稱，而且您可以自動指派 POD。

## 後續步驟

在您檢閱及決定部署選項之後，即可佈建虛擬伺服器。若要開始使用，請參閱[佈建專用主機及實例](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)。
