---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 設定使用者許可權進行自動調整
{: #user-permissions-required-to-use-auto-scale}

存取自動調整選項時，需要除了訂購及管理 {{site.data.keyword.virtualmachinesshort}} 之外的特殊使用者許可權。為了能夠存取自動調整特性，除了已新增的所有未來虛擬裝置之外，您還必須具有管理帳戶上所有虛擬伺服器的許可權。

如果您是帳戶管理者，且想要授與使用者存取自動調整選項的許可權，請完成下列步驟：

1. 在 {{site.data.keyword.cloud}} 主控台中，登入[存取 (IAM) ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/iam#/users){: new_window} 頁面。 
2. 在**使用者**標籤中，選取**檢視者：我的標準基礎架構使用者**。
3. 選取一位使用者，然後按一下**標準基礎架構**標籤。
4. 展開**許可權標籤**中的**裝置**種類，然後選取**管理自動調整群組**。
5. 按一下**套用**。

## 後續步驟

在您有權存取及使用自動調整選項之後，即已備妥可使用此特性。若要開始使用，請檢閱下列資訊：

1. [使用排程型自動調整來管理資料流量激增](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [使用資源型自動調整來管理資料流量激增](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [常見問題：自動調整](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

