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

# 公用虛擬伺服器
公用 {{site.data.keyword.BluVirtServers}} 供應項目是 IBM 受管理、多方承租戶虛擬伺服器部署。它們可讓您擁有預先定義大小的快速可調整性及較高成本有效性，而這些預先定義大小符合可讓您快速啟動並執行的所有商業需求。公用虛擬伺服器有許多優點（包括下列項目）：

* **全球可用性** 

    全球各資料中心都提供公用虛擬伺服器供應項目。

* **配置選項、快速部署及可調整性** 

    公用虛擬伺服器供應項目可提供小型或大型虛擬伺服器選項，以符合各種工作負載需求。

**附註：**如果您要尋找單一承租戶環境，請考慮使用[專用虛擬伺服器](../vsi/vsi_dedicated.html)供應項目。
{:shortdesc}

公用實例位於與其他用戶端共用的 Hypervisor 上。不過，處理器及記憶體專用於虛擬伺服器，讓伺服器效能更為可靠。 

下列是可用的公用虛擬伺服器。 

|公用虛擬伺服器  |說明                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[平衡](../vsi/vsi_public_balanced.html) |最適合需要效能及可調整性平衡的一般雲端工作負載。使用網路連結的儲存空間。|
|[平衡本端儲存空間](../vsi/vsi_public_balanced_local.html) |最適合需要高或低延遲 I/O 效能的大型資料庫叢集。|
|[計算](../vsi/vsi_public_compute.html) |最適合中到高 Web 資料流量工作負載。|
|[記憶體](../vsi/vsi_public_memory.html)  |最適合記憶體快取及即時分析工作負載。
|[GPU](../vsi/vsi_public_gpu.html)  |最適合高效能工作負載。
{: caption="表 1. 支援的公用虛擬伺服器" caption-side="top"}

## 後續步驟

在您檢閱及決定虛擬伺服器特性之後，即可佈建公用虛擬伺服器。若要開始使用，請檢閱下列資訊： 
1. [佈建選項](../vsi/vsi_public_selections.html)
2. [佈建公用實例](../vsi/vsi_provision_public.html)
