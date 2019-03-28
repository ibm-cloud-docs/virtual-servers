---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

keywords: transient virtual servers, transient instances, transient offering, cost savings

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 暫時性虛擬伺服器
{: #about-vs-transient}
如果您有彈性的工作負載，而且想要節省成本，則 {{site.data.keyword.BluVirtServers}} 暫時性供應項目是不錯的選項。在暫時性虛擬伺服器上執行您的工作負載，即可省錢。有未用的容量可用時，會佈建暫時性實例。因此，完整隨選帳戶需要資料中心資源時，您也可能會遺失這些資源。需要收回這些資源時，會根據先開啟先關閉的原則取消供應暫時性實例。   

暫時性虛擬伺服器提供下列彈性：

* **全球可用性**

    全球各資料中心都提供暫時性虛擬伺服器供應項目。

* **節省成本**

    暫時性虛擬伺服器十分適合非正式作業工作負載。例如，您可能會使用暫時性實例來測試及開發應用程式，或在不需要固定執行時間的環境中測試可擴充性。

暫時性實例是使用 SAN 支援的儲存空間的公用實例。

## 通知
資源可用於暫時性實例時，您可以使用 {{site.data.keyword.slapi_short}} 來接收通知。資源變成可用時，您也可以使用 API 以程式設計方式佈建暫時性虛擬伺服器。同樣地，資源變成無法使用時，您可以使用 API 以程式設計方式停止佈建實例。如需相關資訊，請參閱[配置自動化收回通知](/docs/vsi?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers)。

## 限制
在佈建暫時性虛擬伺服器之前，請考量下列限制。

* 支援的並行實例數目是您帳戶層面裝置配額的一部分。如需並行實例限制的相關資訊，請參閱[常見問題：虛擬伺服器](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#concurrent)。
* 無法升級或降級暫時性實例。
* 不需要通知，隨時可以收回資源。
* 暫時性實例無法使用本端儲存空間。
* 暫時性實例只會使用 SAN 支援的儲存空間（平衡式、運算、記憶體）。
* 暫時性實例無法使用 GPU 型設定檔。


## 後續步驟

在您檢閱及選取虛擬伺服器特性之後，即可佈建暫時性虛擬伺服器。若要開始使用，請檢閱下列資訊：
1. [佈建選項](/docs/vsi?topic=virtual-servers-provisioning-selections)
2. [佈建暫時性實例](/docs/vsi?topic=virtual-servers-ordering-vs-transient)
