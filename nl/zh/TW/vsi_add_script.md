---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 新增自訂佈建 Script
{: #adding-post-script}

自訂佈建 Script 可讓使用者指定在新佈建裝置上執行之 Script 的 URL。您可以在 {{site.data.keyword.slportal_full}} 內張貼及管理自訂佈建 Script。
{:shortdesc}

訂購裝置時，您可以選取自訂佈建 Script（如果已張貼到 {{site.data.keyword.slportal}} 的「佈建 Script」畫面）。如果尚未新增 Script，您可以提供 URL。佈建 Script 可以是作業系統 (OS) 可執行的任何檔案（包括結合的二進位檔或任何 OS 支援的語言）。請使用下列步驟，以在 {{site.data.keyword.slportal}} 上新增自訂佈建 Script。

**附註：**目前只有 Linux 及 Unix 型作業系統才提供此特性。

## 新增佈建 Script

1. 從 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 的**裝置**功能表中，選取**管理** > **佈建 Script**。
2. 按一下**新增佈建 Script**。
4. 在「名稱」欄位中，輸入唯一 Script 名稱。
5. 在 URL 欄位中，輸入要與 Script 相關聯的確切 URL。
6. 按一下**新增**。

## 後續步驟
提交包含佈建 Script 的訂單之後，裝置的佈建方式會與任何其他裝置類似。裝置變成可用之前，會將指定的 Script 下載至裝置。佈建 Script 的出處可決定在佈建處理程序的這個最後一個步驟期間的行為。如果 Script 是從 HTTPS URL 提供，則會下載 Script，並在使用者不需要進行額外互動的情況下執行。如果透過 HTTP 提供 Script，則只會下載 Script。針對透過 HTTP 所提供的 Script，管理者必須手動登入裝置並執行 Script。
