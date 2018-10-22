---

copyright:
  years: 2016, 2018

lastupdated: "2018-09-12"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Activity Tracker 事件 
{: #at_events}

身為安全性管理者、審核員或管理員，您可以使用 {{site.data.keyword.cloudaccesstrailfull}} 服務來追蹤使用者及應用程式在 {{site.data.keyword.Bluemix}} 中與虛擬伺服器實例 (VSI) 互動的情形。與帳戶鏈結的帳戶擁有者及使用者，可以觸發虛擬伺服器事件，這些事件會記錄在 {{site.data.keyword.cloudaccesstrailshort}} 中。{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} 服務會記錄由使用者起始，且會變更 {{site.data.keyword.Bluemix_notm}} 中服務狀態的活動。如需相關資訊，請參閱[關於 {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov )。

若要開始監視使用者的動作，請參閱 [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla)。 

起始者可以是使用者、服務或應用程式。若要讓使用者產生事件，使用者必須能夠在 {{site.data.keyword.Bluemix}} 主控台中存取**基礎架構**資源。
{: tip}

## 登入事件
{: #login}

下表列出會產生登入事件的動作：

| 動作 |說明                                                                                              |
|----------|---------|
| `audit-log.user.login`  |起始者透過 {{site.data.keyword.Bluemix}} 使用者介面或 {{site.data.keyword.slportal}} 登入 {{site.data.keyword.Bluemix}} 時，會產生事件。| 
{: caption="表 1. 登入動作" caption-side="top"} 


## 虛擬伺服器實例事件
{: #vsi}

您可以使用 {{site.data.keyword.cloudaccesstrailshort}} 服務，在虛擬伺服器實例 (VSI) 的生命週期中審核它。

下表列出會產生事件的動作：

| 動作 |說明                                                                                              |
|----------|---------|
| `audit-log.vsi.provision`             | 起始者佈建 VSI 時，會產生事件。| 
| `audit-log.vsi-port.disable`          | 起始者停用 VSI 中的埠時，會產生事件。| 
| `audit-log.vsi-port.enable`           | 起始者啟用 VSI 中的埠時，會產生事件。| 
| `audit-log.vsi-port-speed.update`     | 起始者更新 VSI 中的埠速度時，會產生事件。|
| `audit-log.vsi-image-template.create` | 起始者建立 VSI 的映像檔範本時，會產生事件。|
| `audit-log.vsi.power-off`             | 起始者關閉 VSI 電源時，會產生事件。|
| `audit-log.vsi.soft-power-off`        | 起始者在 VSI 上執行正常關閉電源時，會產生事件。|
| `audit-log.vsi.force-power-off`       | 起始者在 VSI 上執行強制關閉電源時，會產生事件。|
| `audit-log.vsi.reboot`                | 起始者將 VSI 重新開機時，會產生事件。| 
| `audit-log.vsi.soft-reboot`           | 起始者在 VSI 上執行正常重新開機時，會產生事件。| 
| `audit-log.vsi.hard-reboot`           | 起始者在 VSI 上執行強迫重新開機時，會產生事件。| 
| `audit-log.vsi.power-on`              | 起始者開啟 VSI 電源時，會產生事件。| 
| `audit-log.vsi.rename`                | 起始者重新命名 VSI 時，會產生事件。| 
| `audit-log.vsi.rescue`                | 起始者救援 VSI 時，會產生事件。| 
| `audit-log.vsi-security-group.add`    | 起始者將安全群組新增至 VSI 時，會產生事件。| 
| `audit-log.vsi-security-group.remove` |起始者從 VSI 移除安全群組時，會產生事件。| 
| `audit-log.vsi.reload`                | 起始者執行 VSI 的作業系統 (OS) 重新載入時，會產生事件。| 
| `audit-log.vsi.boot`                  | 起始者從映像檔啟動 VSI 時，會產生事件。| 
| `audit-log.vsi.reclaim`               | 起始者取消 VSI 時，會產生事件。| 
| `audit-log.vsi.pause`                 | 起始者暫停 VSI 時，會產生事件。| 
{: caption="表 2. VSI 動作" caption-side="top"} 



## 檢視事件
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} 事件提供於事件產生所在之 {{site.data.keyword.Bluemix_notm}} 地區中可用的 {{site.data.keyword.cloudaccesstrailshort}} **帳戶網域**。如需相關資訊，請參閱[檢視帳戶事件](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events)。

{{site.data.keyword.cloudaccesstrailshort}} 事件會自動轉遞至動作發生所在之相同地區的 {{site.data.keyword.cloudaccesstrailshort}} 服務中。
