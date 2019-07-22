---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# 從協力廠商映像檔佈建虛擬伺服器實例
{: #ordering-3P}

您可以從協力廠商供應商建立的映像檔佈建虛擬伺服器實例。您可以透過 {{site.data.keyword.cloud}} 型錄「雲端映像檔」鏈結，來取得協力廠商映像檔。
{:shortdesc}

## 開始之前
開始之前，請確定您已設定 {{site.data.keyword.cloud_notm}} 型錄認證。

針對 {{site.data.keyword.Bluemix_notm}} 型錄，您必須具有已升級的帳戶，才能訂購虛擬伺服器。如需升級帳戶的相關資訊，請參閱[切換至 IBM ID](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)。
{:note}

## 選取虛擬伺服器映像檔
1. 使用唯一認證來登入 [{{site.data.keyword.cloud_notm}} 型錄 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/catalog/){: new_window}。
2. 在**雲端映像檔**區段中，尋找並按一下您要部署的協力廠商映像檔。
3. 檢閱自訂映像檔詳細資料，然後按一下**繼續**。即會顯示**虛擬伺服器實例 - 自訂映像檔**頁面，並預先選取您的自訂映像檔。

## 檢閱及選擇您的部署選項
如需相關資訊，請參閱下列主題：

|部署選項                                     |說明                                               |
| --------------------------------------------------------- | --------------------------------------------------- |
|[公用虛擬伺服器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)                   |IBM 受管理、多方承租戶虛擬伺服器部署|
|[暫時性虛擬伺服器](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)|以較低成本且最適合彈性工作負載而提供的 IBM 受管理、多方承租戶虛擬伺服器部署|
|[保留虛擬伺服器](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)  |由 IBM 管理的多方承租戶虛擬伺服器部署，具在合約期間內具有保證容量|
|[專用虛擬伺服器](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)                |IBM 受管理、單一承租戶虛擬伺服器部署 |
{: caption="表 1. 部署選項" caption-side="top"}

## 佈建虛擬伺服器
在您決定部署選項之後，請開始佈建處理程序。如需相關資訊，請參閱下列主題。

因為您已使用自訂映像檔來啟動佈建處理程序，所以在佈建過程中，您無法變更映像檔類型。
{:note}

|              佈建指示                                         |說明                                                   |
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[佈建公用實例](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)                                 |使用各種選項佈建公用實例                                    |
|[佈建暫時性實例](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)                |使用各種選項佈建暫時性實例                                    |
|[佈建保留容量及實例](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)            |使用各種選項佈建保留容量及實例|
|[佈建專用主機及實例](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)|在專用主機上佈建專用實例 (private instance) 或專用實例 (dedicated instance)                                  |
{: caption="表 2. 佈建資訊" caption-side="top"}


## 後續步驟
虛擬伺服器在佈建且可供使用之後，即可使用 {{site.data.keyword.cloud_notm}} 主控台或 {{site.data.keyword.slapi_short}} 來配置虛擬伺服器。如需相關資訊，請參閱[配置虛擬伺服器](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)。
