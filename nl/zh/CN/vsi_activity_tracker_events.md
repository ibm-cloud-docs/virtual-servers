---

copyright:
  years: 2016, 2018
lastupdated: "2018-11-06"

subcollection: virtual-servers

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

作为安全主管、审计员或管理者，您可以使用 {{site.data.keyword.cloudaccesstrailfull}} 服务来跟踪用户和应用程序与 {{site.data.keyword.Bluemix}} 中的虚拟服务器实例 (VSI) 的交互情况。帐户所有者以及与该帐户链接的用户可以触发在 {{site.data.keyword.cloudaccesstrailshort}} 中记录的虚拟服务器事件。
{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} 服务会记录用户启动的更改 {{site.data.keyword.Bluemix_notm}} 中服务状态的活动。有关更多信息，请参阅[关于 {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov )。

要开始监视用户操作，请参阅 [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started-with-cla#getting-started-with-cla)。

发起者可以是用户、服务或应用程序。要使用户能够生成事件，该用户必须有权在 {{site.data.keyword.Bluemix}} 控制台中访问**基础架构**资源。
{: tip}

## 虚拟服务器实例事件
{: #vsi}

您可以使用 {{site.data.keyword.cloudaccesstrailshort}} 服务在虚拟服务器实例 (VSI) 对生命周期内对其进行审计。

下表列出了生成事件的操作：

|操作|描述|
|----------|---------|
|`audit-log.vsi.provision`|发起者供应 VSI 时，会生成事件。|
|`audit-log.vsi-port.disable`|发起者在 VSI 中禁用端口时，会生成事件。|
|`audit-log.vsi-port.enable`|发起者在 VSI 中启用端口时，会生成事件。|
|`audit-log.vsi-port-speed.update`|发起者在 VSI 中更新端口速度时，会生成事件。|
|`audit-log.vsi-image-template.create`|发起者创建 VSI 的映像模板时，会生成事件。|
|`audit-log.vsi.power-off`|发起者关闭 VSI 的电源时，会生成事件。|
|`audit-log.vsi.soft-power-off`|发起者对 VSI 执行软电源关闭时，会生成事件。|
|`audit-log.vsi.force-power-off`|发起者对 VSI 执行强制电源关闭时，会生成事件。|
|`audit-log.vsi.reboot`|发起者重新引导 VSI 时，会生成事件。|
|`audit-log.vsi.soft-reboot`|发起者对 VSI 执行软重新引导时，会生成事件。|
|`audit-log.vsi.hard-reboot`|发起者对 VSI 执行硬重新引导时，会生成事件。|
|`audit-log.vsi.power-on`|发起者打开 VSI 的电源时，会生成事件。|
|`audit-log.vsi.rename`|发起者对 VSI 重命名时，会生成事件。|
|`audit-log.vsi.rescue`|发起者拯救 VSI 时，会生成事件。|
|`audit-log.vsi-security-group.add`|发起者向 VSI 添加安全组时，会生成事件。|
|`audit-log.vsi-security-group.remove`|发起者从 VSI 中除去安全组时，会生成事件。|
|`audit-log.vsi.reload`|发起者对 VSI 执行操作系统 (OS) 重装时，会生成事件。|
|`audit-log.vsi.boot`|发起者通过映像引导 VSI 时，会生成事件。|
|`audit-log.vsi.reclaim`|发起者取消 VSI 时，会生成事件。|
|`audit-log.vsi.pause`|发起者暂停 VSI 时，会生成事件。|
{: caption="表 2. VSI 操作" caption-side="top"}



## 查看事件
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} 事件在生成这些事件的 {{site.data.keyword.Bluemix_notm}} 区域中可用的 {{site.data.keyword.cloudaccesstrailshort}} **帐户域**中提供。有关更多信息，请参阅 [查看帐户事件](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events)。

{{site.data.keyword.cloudaccesstrailshort}} 事件会自动转发到发生操作的区域中的 {{site.data.keyword.cloudaccesstrailshort}} 服务。
