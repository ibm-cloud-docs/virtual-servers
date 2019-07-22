---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

keywords: transient virtual servers, transient instances, transient offering, cost savings

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 瞬态虚拟服务器
{: #about-vs-transient}
如果您具有灵活的工作负载并且希望节省成本，那么 {{site.data.keyword.BluVirtServers}} 瞬态产品是不错的选择。通过在瞬态虚拟服务器上运行工作负载，可节省资金。存在未使用的容量时，会供应瞬态实例。因此，完全的随需应变帐户需要数据中心资源时，您也可能会失去这些资源。需要回收这些资源时，瞬态实例以先入先出的方式取消供应。   

瞬态虚拟服务器提供以下灵活性：

* **全球可用性**

    瞬态虚拟服务器产品在全球各个数据中心内可用。

* **节约成本**

    瞬态虚拟服务器最适用于非生产工作负载。例如，可使用瞬态实例来测试和开发应用程序，或者在不需要持续正常运行时间的环境中测试可扩展性。

瞬态实例是使用 SAN 支持的存储器的公共实例。以下公共实例系列可用于此产品。

| 系列  |描述|
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[均衡](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced)|最适用于需要均衡性能和可扩展性的常用云工作负载。使用网络连接存储器。|
|[计算](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute)|最适用于中到高 Web 流量工作负载。|
|[内存](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)|最适用于内存高速缓存和实时分析工作负载。
|
{: caption="表 1. 公共虚拟服务器系列选择" caption-side="top"}

## 通知
资源可供瞬态实例使用时，可以使用 {{site.data.keyword.slapi_short}} 来接收通知。资源可用时，还可以使用 API 通过编程方式来供应瞬态虚拟服务器。同样，在资源不可用时，可以使用 API 通过编程方式来停止供应实例。有关更多信息，请参阅[配置自动回收通知](/docs/vsi?topic=virtual-servers-configuring-notifications-for-reclaims-of-transient-virtual-servers#configuring-notifications-for-reclaims-of-transient-virtual-servers)。  

## 限制
在供应瞬态虚拟服务器之前，请考虑以下限制。

* 支持的并发实例数是您的帐户内设备配额的一部分。有关并发实例限制的更多信息，请参阅[常见问题：虚拟服务器](/docs/vsi?topic=virtual-servers-faqs-virtual-servers#faqs-virtual-servers)。
* 瞬态实例无法升级或降级。
* 资源可以随时回收，而无需通知。
* 瞬态实例无法使用本地存储器。
* 瞬态实例无法使用基于 GPU 的概要文件。


## 后续步骤

复查并选择虚拟服务器概要文件之后，即可以供应瞬态虚拟服务器。要开始使用，请参阅[供应瞬态实例](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)。

