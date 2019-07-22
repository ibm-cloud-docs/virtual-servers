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

# 关于自动缩放
{: #about-auto-scale}

通过 {{site.data.keyword.cloud}} 虚拟服务器实例的自动缩放，您能够自动执行与添加或除去实例关联的手动缩放过程，以支持业务应用程序。这允许您在需要更多资源时，自动设置新的实例；在额外负载下降时，关闭并除去这些实例。自动缩放使用组来包含策略，策略可更改环境扩大或缩小的方式。这些策略将根据您的业务和应用程序需求，使用操作来添加或除去虚拟服务器。
{:shortdesc}

自动缩放将启用以下功能：

* 根据需求而需要更多资源时，无缝地自动扩展实例
* 需求下降时，通过除去不必要的资源，从而无缝地自动缩减实例（节省资金）
* 灵活的缩放触发器：CPU 百分比、出局公共和专用带宽以及入局公共和专用带宽
* 针对组中缩放活动的近实时状态更新
* （可选）将虚拟 LAN (VLAN) 和本地负载均衡器相集成

可以应用自动缩放的两种常见业务解决方案：

| 解决方案 |描述|
| -------- | ----------- |
| [基于调度的缩放](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling) |使用此基于调度的缩放可设置针对基于时间的使用量峰值的策略，例如在周末或假日。基于安排的缩放可以在公司预期流量突增的情况下使用；例如，需要基于安排增加资源的社交网络站点。|
| [基于资源的缩放](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling) |使用基于资源的调度可基于资源使用量来设置针对不定期峰值的策略。如果急需将产品推向市场，或电子商务站点要降价销售并且需要资源来维持响应时间，那么将发生不定期流量峰值。|
{: caption="表 1. 自动缩放解决方案" caption-side="top"}

如果您不是帐户管理员，那么您的用户帐户必须包含使用自动缩放的许可权。帐户管理员可以从 {{site.data.keyword.cloud_notm}} 控制台授予用户许可权。有关更新许可权的更多信息，请参阅[设置自动缩放的用户许可权](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale)。
{:note}


