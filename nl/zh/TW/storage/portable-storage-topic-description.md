---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 關於可攜式儲存磁區

可攜式儲存磁區是專用於 {{site.data.keyword.BluVirtServers_short}} 的輔助儲存空間解決方案。它們一次可以連接至一部虛擬伺服器。如果您要在位在 {{site.data.keyword.cloud}} 網路上的任何資料中心內的虛擬伺服器之間傳送資料，它們也是理想的解決方案。可攜式儲存磁區適用需要存取原始、未格式化區塊層次儲存空體的資料庫應用程式，也適合在 {{site.data.keyword.BluVirtServers_short}} 之間移動大型資料集。

當可攜式儲存磁區連接至與原始虛擬伺服器不同的資料中心內的虛擬伺服器時，{{site.data.keyword.cloud}} 的內部系統會將磁區複製到新資料中心內的 SAN。然後系統會驗證所複製磁區的完整性，並從原始資料中心 SAN 移除原始可攜式磁區。

## 後續步驟
如需如何使用可攜式儲存磁區的相關資訊，請參閱下列作業：
* [存取可攜式儲存空間](/docs/vsi/storage?topic=virtual-servers-accessing-portable-storage)
* [編輯可攜式儲存空間說明](/docs/vsi/storage?topic=virtual-servers-editing-a-portable-storage-description)
