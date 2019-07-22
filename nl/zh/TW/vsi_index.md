---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: virtual servers, provisioning process, IBM Cloud Virtual Servers

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 入門指導教學
{: #getting-started-tutorial}

您可以在幾分鐘之內部署 {{site.data.keyword.BluVirtServers}}。虛擬伺服器是從您選擇的虛擬伺服器映像檔中進行部署，並部署在對工作負載有意義的地理區域中。
{:shortdesc}

請在虛擬專用雲端上試用我們的虛擬伺服器！如需相關資訊，請參閱 [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started)。
{:tip}

當您在標準基礎架構中建立虛擬伺服器時，可以選擇公用（多方承租戶）環境或專用（單一承租戶）環境。然後，根據選擇的環境，您也必須選取每小時、每月或暫時性虛擬伺服器。如果是公用虛擬伺服器，則您也可以選擇使用 SAN 型儲存空間或本端儲存空間。

## 開始之前

開始之前，請檢閱下列必要條件。

  1. 您必須具有已升級的帳戶，才能訂購虛擬伺服器。此處理程序可能需要一些時間，並且需要先核准要求，才能繼續進行。如需升級帳戶的相關資訊，請參閱[切換至 IBM ID](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)。
  2. 檢閱及選擇部署選項。如需相關資訊，請參閱下列主題：

|部署選項                                     |說明                                               |
| --------------------------------------------------------- | --------------------------------------------------- |
|[公用虛擬伺服器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)                   |IBM 受管理、多方承租戶虛擬伺服器部署|
|[暫時性虛擬伺服器](/docs/vsi?topic=virtual-servers-about-vs-transient)|以較低成本且最適合彈性工作負載而提供的 IBM 受管理、多方承租戶虛擬伺服器部署|
|[保留虛擬伺服器](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers)  |由 IBM 管理的多方承租戶虛擬伺服器部署，具在合約期間內具有保證容量|
|[專用虛擬伺服器](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)                |IBM 受管理、單一承租戶虛擬伺服器部署 |
{: caption="表 1. 部署選項" caption-side="top"}   

## 佈建虛擬伺服器

在您決定部署選項之後，請開始佈建處理程序。

|              佈建指示                                         |說明                                                   |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[佈建公用實例](/docs/vsi?topic=virtual-servers-ordering-vs-public)                                 |使用各種選項佈建公用實例                                    |
|[佈建暫時性實例](/docs/vsi?topic=virtual-servers-ordering-vs-transient)                |使用各種選項佈建暫時性實例                                    |
|[佈建保留容量及實例](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances)            |使用各種選項佈建保留容量及實例|
|[佈建專用主機及實例](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)|在專用主機上佈建專用實例 (private instance) 或專用實例 (dedicated instance)|
{: caption="表 2. 佈建資訊" caption-side="top"}

## 後續步驟

虛擬伺服器在佈建且可供使用之後，即可使用 {{site.data.keyword.cloud_notm}} 主控台或 {{site.data.keyword.slapi_short}} 來配置虛擬伺服器。如需相關資訊，請參閱[配置虛擬伺服器](/docs/vsi?topic=virtual-servers-configuring-virtual-servers)。
