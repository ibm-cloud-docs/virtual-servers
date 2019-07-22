---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords: auto scale, virtual servers

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 關於自動調整
{: #about-auto-scale}

{{site.data.keyword.cloud}} 虛擬伺服器實例的自動調整可讓您自動化手動調整處理程序，而此處理程序與新增或移除實例來支援商業應用程式相關聯。這可讓您在需要更多資源時自動設定新實例，然後在額外負載減弱時關閉並刪除這些實例。自動調整會使用群組來包含可變更環境之擴充或收縮方式的原則。這些原則會使用動作，根據您的商業及應用程式需求來新增或移除虛擬伺服器。
{:shortdesc}

自動調整會啟用下列特性：

* 因需求而需要更多資源時，無縫及自動擴增實例
* 需求降低（省錢）時，藉由移除不必要的資源來無縫及自動縮減實例
* 彈性調整觸發程式：CPU 百分比、送出的公用和專用頻寬，以及送入的公用和專用頻寬
* 調整群組中活動的接近即時狀態更新
* 選用整合虛擬 LAN (VLAN) 及本端負載平衡器

以下是兩種可將自動調整套用至其中的常用商業解決方案：

| 解決方案 |說明                                                                                              |
| -------- | ----------- |
| [排程型調整](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling) | 排程型調整可用來設定時間型用量激增的原則，例如週末或假日。當公司預期資料流量激增時，例如根據排程需要更多資源的社交網站，可以使用以排程為基礎的調整。|
| [資源型調整](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling) | 根據資源用量，資源型排程可以用來設定不規則激增的原則。當推送產品進入市場或電子商務網站正在進行銷售，並且需要資源來維持回應時間時，資料流量可能會出現不規則的激增。|
{: caption="表 1. 自動調整解決方案" caption-side="top"}

如果您不是帳戶管理者，則您的使用者帳戶必須包含許可權，才能使用自動調整。帳戶管理者可以從 {{site.data.keyword.cloud_notm}} 主控台中授與使用者的許可權。如需更新許可權的相關資訊，請參閱[設定使用者許可權進行自動調整](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale)。{:note}


