---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 管理可攜式儲存空間
{: #accessing-portable-storage}

「可攜式儲存空間磁區 (PSV)」是一種專門用於 {{site.data.keyword.virtualmachinesshort}} 的輔助儲存空間解決方案。在 {{site.data.keyword.cloud}} 主控台內，您可以存取可攜式儲存空間磁區，並顯示所有 PSV。您也可以連接、分離、交換及編輯磁區。
{:shortdesc}

您無法將可攜式儲存空間磁區連接或交換至從已加密映像檔範本佈建的虛擬伺服器實例。
{:note}

## 開始之前
首先，導覽至儲存空間或裝置功能表，並確定您具有完成作業所需的正確帳戶許可權。

* 導覽至主控台的儲存空間或裝置功能表。如需相關資訊，請參閱[導覽至裝置](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 確保您具有任何必要的帳戶許可權及裝置存取權。只有帳戶擁有者或具有**管理使用者**標準基礎架構許可權的使用者才能調整許可權。

如需許可權的相關資訊，請參閱[傳統基礎架構許可權](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理裝置存取權](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 連接可攜式儲存空間

1. 從**儲存空間**功能表中，選取 **Block Storage**。
2. 在**可攜式儲存空間**區段中，選取您要使用之可攜式儲存空間的連接選項。
3. 在下一個畫面上，選擇需要儲存空間的裝置，然後選取**連接**。

## 管理連接至伺服器的可攜式儲存空間

連接至伺服器的可攜式儲存空間會列在伺服器的*裝置詳細資料* 頁面中。

1. 從**裝置**功能表中，選取**裝置清單**。
2. 從**裝置清單**中，選取虛擬伺服器實例，以檢視其詳細資料。
3. 按一下**儲存空間**標籤，以檢視目前連接至實例的可攜式儲存空間。
4. 在**動作**功能表中，您可以**交換**或**分離**儲存空間。
