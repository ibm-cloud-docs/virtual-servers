---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 備份服務
{: #back-up-services}

## IBM Cloud Backup

{{site.data.keyword.backup_full}} 是一種透過 {{site.data.keyword.backup_notm}} WebCC 瀏覽器型管理公用程式所管理的自動化代理程式型備份系統，並提供一種方法，讓使用者備份 {{site.data.keyword.BluSoftlayer}} 網路的一個以上資料中心內伺服器之間的資料。管理者可以設定備份，使其遵循已將目標設為完整系統、特定目錄或甚至個別檔案的每小時、每日、每週或自訂排程。其他外掛程式容許與軟體（例如 Microsoft Exchange 及 Microsoft SQL）及其他類型的協力廠商軟體相容，並讓使用者執行「裸機還原」（必要時）。

如需 {{site.data.keyword.backup_notm}} 服務的相關資訊，請參閱[開始使用 {{site.data.keyword.backup_notm}} 服務](/docs/infrastructure/Backup?topic=Backup-gettingstarted#gettingstarted)。

## R1Soft CDP

「持續資料保護 (CDP)」是 R1Soft 所建立的高效能備份軟體，容許同時備份實體及虛擬裝置。Idera CDP 包含三個主要元件：CDP 伺服器、代理程式，以及資料庫外掛程式（可與前兩個元件分開購買）。因為 R1Soft CDP 是一種協力廠商備份解決方案，所以與 CDP 的互動完全是在 {{site.data.keyword.Bluemix_short}} 專有介面外部進行；不過，R1Soft CDP 密碼可能在 {{site.data.keyword.slportal}} 內進行追蹤及儲存。R1Soft 網站會記載與 R1Soft CDP 的所有其他互動。

如需 R1Soft CDP 備份服務的相關資訊，請參閱 [R1Soft 文件 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://wiki.r1soft.com/display/ServerBackupManager/Home){: new_window}。
