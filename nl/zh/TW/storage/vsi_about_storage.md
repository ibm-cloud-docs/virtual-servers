---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-26"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 儲存空間選項

您可以為每一部虛擬伺服器選擇 SAN 或本端儲存空間。您可以視需要使用其他儲存產品補充 SAN 或本端儲存空間。 

## 本端儲存空間

本端儲存空間是在虛擬伺服器主機的本端磁碟上進行建置。本端儲存空間提供改良的磁碟讀寫效能。磁碟是以多磁碟機陣列 (RAID) 配置所建置，可進行由 {{site.data.keyword.cloud}} 完全管理的備援、磁碟更換及性能監視。在較新的資料中心內，此儲存空間是可提供最佳效能的所有固態硬碟 (SSD)。 

## SAN 儲存空間
 
SAN 儲存空間是以 {{site.data.keyword.cloud_notm}} 的 SAN 基礎架構為建置基礎，而不是本端主機儲存空間。這可以在主機故障時提供更大的備援，也可以支援更大的磁區。如果主機故障，則會將使用 SAN 型儲存空間的虛擬伺服器實例自動移轉至其他主機，並重新啟動。 

所有次要磁碟都會連接為可攜式儲存空間。在大部分案例中，您隨時可以分離磁碟，以將它們移至其他虛擬伺服器。 

**例外狀況：**如果是使用平衡本端儲存空間的公用虛擬伺服器，則無法分離主要或次要磁碟。

只要變更未超出目標虛擬伺服器的磁碟限額或磁區大小上限，即可將磁碟重新連接至另一部伺服器。

**附註：**已移動的磁碟會轉換成目標伺服器的儲存空間類型。

## 可攜式儲存磁區

可攜式儲存磁區是專用於 {{site.data.keyword.BluVirtServers_short}} 的輔助儲存空間解決方案。它們一次可以連接至一部虛擬伺服器。如果您要在位在 {{site.data.keyword.cloud_notm}} 網路上的任何資料中心內的虛擬伺服器之間傳送資料，它們也是理想的解決方案。可攜式儲存磁區適用需要存取原始、未格式化區塊層次儲存空體的資料庫應用程式，也適合在 {{site.data.keyword.BluVirtServers_short}} 之間移動大型資料集。

當可攜式儲存磁區連接至與原始虛擬伺服器不同的資料中心內的虛擬伺服器時，{{site.data.keyword.cloud_notm}} 的內部系統會將磁區複製到新資料中心內的 SAN。然後系統會驗證所複製磁區的完整性，並從原始資料中心 SAN 移除原始可攜式磁區。

## LVM 限制

不支援將邏輯磁區管理 (LVM) 作為可開機分割方法。藉由適當的作業系統支援及配置，可以將次要虛擬伺服器磁碟用於 LVM 分割區。不過，LVM 不是「映像檔範本」或「Flex 映像檔」支援的檔案系統。

## 補充儲存空間

虛擬伺服器與檔案和區塊 SAN 儲存空間以及物件儲存空間完全相容。建議將這些儲存空間類型用於叢集磁碟機、共用檔案儲存空間、保存儲存空間、大型儲存空間需求或特定效能需求。

如需補充性儲存空間選項的相關資訊，請參閱下列資源：

* [開始使用 Block Storage](/docs/infrastructure/BlockStorage/index.html)
* [開始使用 File Storage](/docs/infrastructure/FileStorage/index.html)
* [開始使用 Object Storage](/docs/services/ObjectStorage/index.html)

## 後續步驟
如需如何使用可攜式儲存磁區的相關資訊，請參閱下列作業：
* [存取可攜式儲存空間](../storage/access-portable-storage-screen.html)
* [編輯可攜式儲存空間說明](../storage/edit-description-portable-storage-volume-psv.html)


