---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:note: .note}
{:new_window: target="_blank"}

# 管理放置群組
{: #vsi_managing_placegroup}

您可以使用 {{site.data.keyword.cloud}} 主控台中的放置群組頁面或裝置詳細資料頁面，來管理放置群組。
{:shortdesc}

## 新增放置群組

若要從放置群組頁面新增放置群組，請完成下列步驟：
{:shortdesc}

1. 開啟[放置群組 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} 頁面。
2. 在放置群組頁面上，按一下**新建群組**。
3. 輸入放置群組的名稱、位置、Pod 及規則，然後按一下**建立**。

現有的實例無法新增至放置群組；您只能在佈建時將虛擬伺服器實例新增至放置群組。{:note}

## 管理放置群組

若要從放置群組頁面管理放置群組，請完成下列步驟：
{:shortdesc}

1. 開啟[放置群組 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/gen1/infrastructure/placement-groups){: new_window} 頁面。
2. 在放置群組區段下，您可以完成數項管理作業。
     * 檢視放置群組的清單及已指派的實例數
     * 新增群組
     * 重新命名群組
     * 佈建實例
     * 刪除群組
     
您必須從放置群組中移除已指派的伺服器，才能刪除放置群組。若要從放置群組移除實例，您必須刪除或收回實例。{:note}
