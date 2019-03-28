---

copyright:
  years: 2014, 2018
lastupdated: "2018-04-27"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 管理佈建 Script
{: #managing-a-provisioning-script}

使用佈建 Script，以指定要在新佈建裝置上執行之 Script 的 URL。Script 名稱沒有任何限制；不過，對每一個 Script 使用類似的命名慣例，可以方便識別。佈建 Script 必須與完整網域名稱相關聯，並且可以使用 HTTP 或 HTTPS 通訊協定進行存取。使用的通訊協定類型會影響系統在將佈建 Script 下載至裝置時的自動回應。

* 使用 **HTTP 通訊協定**需要管理者在下載 Script 之後手動執行 Script。
* 使用 **HTTPS 通訊協定**會自動下載及執行 Script（可能的話）。如果 URL 未與可執行 Script 相關聯，則會下載 Script，而且不需要採取任何進一步動作。

## 存取佈建 Script 畫面
1. 使用唯一認證來進入 [{{site.data.keyword.slportal_full}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window}。
2. 從導覽中選取**裝置 > 管理 > 佈建 Script**，以存取「佈建 Script」畫面。


## 新增佈建 Script
{: #add-provisioning-script}

1. 從 {{site.data.keyword.slportal}} 中的**佈建 Script** 畫面，按一下畫面頂端的**新增佈建 Script**。
* 在**名稱**欄位中，輸入佈建 Script 的**識別性名稱**。
* 在 **URL** 欄位中，輸入與 Script 相關聯的**完整網域名稱**。
* 按一下**新增**，以將佈建 Script 新增至帳戶。按一下**取消**，以取消動作。

## 編輯佈建 Script 詳細資料

1. 從 {{site.data.keyword.slportal}} 的**佈建 Script** 畫面中，按一下佈建 Script 之**名稱**或 **URL** 直欄中的任意處，以開啟 Script 進行編輯。
3. 更新名稱或 URL。
  * **附註：**當您更新 URL 時，必須使用完整網域名稱，否則不會儲存變更。
4. 按一下畫面上的任意處，以儲存編輯。

## 後續步驟

您隨時可以修改或移除與帳戶相關聯的佈建 Script。佈建 Script 在移除之前都會儲存在 {{site.data.keyword.slportal}} 中，而且可以與透過 {{site.data.keyword.slportal}} 訂購的任何新裝置相關聯。如果 Script 與 HTTP URL 相關聯，則會在佈建期間將它下載至新的裝置。會下載與 HTTPS URL 相關聯的 Script，並在適當時於新的裝置上執行。

在您編輯 Script 之後，會立即在畫面上顯示有效的更新項目。變更現有佈建 Script 並不會影響已佈建的裝置。
