---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 公用虛擬伺服器
{: #about-public-virtual-servers}

公用 {{site.data.keyword.BluVirtServers}} 供應項目是 IBM 受管理、多方承租戶虛擬伺服器部署。它們可讓您擁有預先定義大小的快速可調整性及較高成本有效性，而這些預先定義大小符合可讓您快速啟動並執行的所有商業需求。
{:shortdesc}

公用虛擬伺服器有許多優點（包括下列項目）：

* **全球可用性** 

    全球各資料中心都提供公用虛擬伺服器供應項目。

* **配置選項、快速部署及可調整性** 

    公用虛擬伺服器供應項目可提供小型或大型虛擬伺服器選項，以符合各種工作負載需求。

無法保證公用虛擬伺服器的網路資料流量（其包含 VSI SAN 及其他網路連接的儲存空間）。如果虛擬伺服器實例的網路資料流量開始對其他虛擬伺服器有明顯且負面的影響，則可能要在新的主機上重新啟動該實例，或者，在極端的情況下完全予以停用。此負面影響通常會以資料流量層次接近每秒 20,000 到 30,000 個封包 (PPS) 的方式觀察到。針對保證的網路，建議使用「專用虛擬伺服器」供應項目。如需相關資訊，請參閱單一承租戶環境：[專用虛擬伺服器](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)供應項目。

下列系列的公用實例適用於此供應項目。 

| 系列  |說明                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[平衡](/docs/vsi?topic=virtual-servers-balanced#balanced) |最適合需要效能及可調整性平衡的一般雲端工作負載。使用網路連結的儲存空間。|
|[平衡本端儲存空間](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) |最適合需要高 I/O 效能且延遲很低的大型資料庫工作負載。|
|[計算](/docs/vsi?topic=virtual-servers-compute#compute) |最適合中到高 Web 資料流量工作負載。|
|[記憶體](/docs/vsi?topic=virtual-servers-memory#memory)  |最適合記憶體快取及即時分析工作負載。
|
|[GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  |最適合高效能工作負載。
{: caption="表 1. 公用虛擬伺服器系列選項" caption-side="top"}

這些系列有部分也可用於 IBM Cloud Virtual Servers for VPC。如需相關資訊，請參閱 [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started)。
{:tip}

## 後續步驟

在您檢閱及決定虛擬伺服器設定檔之後，即可佈建公用虛擬伺服器。若要開始，請參閱[佈建公用實例](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)。
