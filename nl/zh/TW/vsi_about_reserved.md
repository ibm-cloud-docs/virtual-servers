---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-25"

keywords: reserved virtual servers, cost savings, guaranteed capacity 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 保留虛擬伺服器  
{: #about-reserved-virtual-servers}

如果您要未來的部署能有保證的資源並且節省成本，則 {{site.data.keyword.BluVirtServers}} 保留實例供應項目是不錯的選項。您可以針對保留容量選擇一年或三年的合約期間。在該保留容量內，您可以保留一組特定大小且最多 20 個的虛擬伺服器實例，然後在需要這些實例時進行佈建。在合約期間的期限內，會保證您在選擇的 POD 及資料中心內擁有此容量。

保留虛擬伺服器實例提供許多優點，包括如下：

* **保證容量**

    當您保留容量時，在合約期間的期限內會保證此容量。 
    
* **全球可用性**
    
    全球各資料中心都提供保留虛擬伺服器供應項目。

* **可靠的佈建**
   
   您隨時可以佈建及收回虛擬伺服器實例的保留容量。

* **節省成本**
    
    與按小時或按月的虛擬伺服器計費週期相較之下，選擇一年或三年的合約期間可容許一致的每月付款及較低成本。

保留的虛擬伺服器實例是使用 SAN 支援的儲存空間的公用實例。下列系列的公用實例適用於此供應項目。

| 系列  |說明                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[平衡](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) |最適合需要效能及可調整性平衡的一般雲端工作負載。使用網路連結的儲存空間。|
|[計算](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) |最適合中到高 Web 資料流量工作負載。|
|[記憶體](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  |最適合記憶體快取及即時分析工作負載。
|
{: caption="表 1. 公用虛擬伺服器系列選項" caption-side="top"}

## 限制 

請先考量下列限制，再保留容量以及佈建保留虛擬伺服器實例：
  
  * 您無法升級或降級實例。
  * 無法取消保留容量；不過，您可以收回該容量中的虛擬伺服器實例。
    
## 通知

在保留虛擬伺服器容量的期間結束之前一個月，您會收到一封電子郵件通知。

## 後續步驟

在您檢閱並決定選項之後，即可佈建保留容量及實例。若要開始使用，請檢閱下列資訊：

   1. [佈建保留容量及實例](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
   2. [常見問題：保留容量及實例](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
