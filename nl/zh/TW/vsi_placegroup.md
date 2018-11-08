---



copyright:
  years: 2018
lastupdated: "2018-10-31"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 放置群組

使用 {{site.data.keyword.BluVirtServers}} 的放置群組，您可以使用公用實例來建立資料中心內的高可用性，或在較大的部署內提供額外的容錯層次。
{:shortdesc}

建立放置群組，然後指派最多 5 個新的虛擬伺服器實例。使用展開的規則，您的每個虛擬伺服器都會佈建在不同的實體主機上。

若要開始建置處理程序，請遵循下列步驟：
 
1. 從您的瀏覽器，開啟 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){:new_window}，然後登入帳戶。
2. 在「放置群組」頁面上，按一下**新增放置群組**。
3. 輸入放置群組的名稱、說明及資料中心，然後按一下**新增**。
4. 找到**訂單**區段，然後按一下**裝置**。
5. 在「裝置」頁面上，針對其中一個「虛擬伺服器」供應項目，按一下**每小時**或**每月**。
6. 完成任何其他必要的資訊，然後按一下**新增至訂單**。即會開啟「結帳」頁面。
7. 您可以選取任何現有的放置群組。**展開**表示實例在不同的實體硬體上。
8. 最後，按一下**提交訂單**。

##限制
現有的實例無法新增至放置群組；您只能在佈建時將虛擬伺服器實例新增至放置群組。 

若要從放置群組移除實例，您必須刪除或收回實例。
     
## 後續步驟

若要建立及管理新的放置群組，請參閱[管理放置群組](vsi_managing_placegroup.html)。
