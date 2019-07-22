---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 管理佈建 Script
{: #managing-a-provisioning-script}

您可以使用佈建 Script，以指定在新佈建裝置上執行之 Script 的 URL。佈建 Script 可以是作業系統 (OS) 可執行的任何檔案，包括結合的二進位檔或任何 OS 支援的語言。Script 名稱沒有任何限制；不過，對每一個 Script 使用類似的命名慣例，可以方便識別。佈建 Script 必須與完整網域名稱相關聯，並且可以使用 HTTP 或 HTTPS 通訊協定進行存取。使用的通訊協定類型會影響系統在將佈建 Script 下載至裝置時的自動回應。  
{:shortdesc}

* 使用 **HTTP 通訊協定**需要管理者在下載 Script 之後手動執行 Script。
* 使用 **HTTPS 通訊協定**會自動下載及執行 Script（可能的話）。如果 URL 未與有效 Script 相關聯，則會下載 Script，而且不需要採取任何進一步動作。

## 開始之前
首先，導覽至裝置功能表，並確定您具有完成作業所需的正確帳戶許可權。 

* 導覽至主控台的裝置功能表。如需相關資訊，請參閱[導覽至裝置](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 確保您具有任何必要的帳戶許可權及裝置存取權。只有帳戶擁有者或具有**管理使用者**標準基礎架構許可權的使用者才能調整許可權。 

如需許可權的相關資訊，請參閱[傳統基礎架構許可權](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理裝置存取權](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 新增佈建 Script
{: #add-provisioning-script}

1. 從**裝置**功能表中，選取**管理 > 佈建 Script**。
2. 選取**新增佈建 Script**。 
3. 在**名稱**欄位中，輸入佈建 Script 的識別性名稱。
4. 在 **URL** 欄位中，輸入與 Script 相關聯的完整網域名稱。
5. 按一下**新增**，以將佈建 Script 新增至帳戶。 

## 編輯佈建 Script 詳細資料
{: #edit-provisioning-script-details}

1. 從**裝置**功能表中，選取**管理 > 佈建 Script**。
2. 按一下佈建 Script 之**名稱**或 **URL** 直欄中的任意處，以開啟 Script 進行編輯。
3. 更新名稱或 URL。當您更新 URL 時，必須使用完整網域名稱，否則不會儲存變更。
   {:note}
4. 按一下畫面上的任意處，以儲存編輯。

## 後續步驟

您隨時可以修改或移除與帳戶相關聯的佈建 Script。佈建 Script 在移除之前都會儲存在 {{site.data.keyword.cloud_notm}} 主控台中，而且可以與透過 {{site.data.keyword.cloud_notm}} 主控台訂購的任何新裝置相關聯。如果 Script 與 HTTP URL 相關聯，則會在佈建期間將它下載至新的裝置，而且管理者必須登入裝置並手動執行 Script。這時會下載與 HTTPS URL 相關聯的 Script，並在適當時於新的裝置上執行，不需任何其他互動。 

如果您編輯 Script，則會立即在畫面上顯示有效的更新項目。變更現有佈建 Script 並不會影響已佈建的裝置。

