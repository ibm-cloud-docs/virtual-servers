---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# 关于暂挂计费
{: #requirements}

关闭支持暂挂计费功能的虚拟服务器时，您不会增加特定计算资源的成本。服务器关闭后会自动停止计费。暂挂计费功能可帮助您降低成本，并使您在再次需要资源时不必重新供应虚拟服务器。
{:shortdesc}

在 2018 年 11 月 1 日之前创建的大部分虚拟服务器实例都不支持暂挂计费功能。要了解自己的虚拟服务器实例是否支持暂挂计费功能，请参阅[查看暂挂计费功能](vsi_viewing_suspend.html)。 

此功能在全球各个数据中心内可用。要供应支持暂挂计费功能的虚拟服务器实例，必须使用下列设置来配置虚拟服务器实例：

* 每小时 SAN
* 以下某一个系列的公共类型模板：
  * 均衡
  * 计算
  * 内存

使用暂挂计费功能可以替代供应和回收虚拟服务器实例，而且速度更快。
{:tip}

仅当通过 {{site.data.keyword.slportal_full}}、CLI 或 {{site.data.keyword.slapi_short}} 关闭虚拟服务器实例的电源时，才会暂停计费。如果是直接通过操作系统来关闭虚拟服务器实例的电源，那么不会暂停对该实例的计费。
{:note}

## 供应详细信息

您可以通过 {{site.data.keyword.cloud_notm}} 目录、CLI 或 {{site.data.keyword.slapi_short}} 来供应支持暂挂计费功能的虚拟服务器实例。有关供应公共虚拟服务器实例的更多信息，请参阅[供应公共实例](../vsi/vsi_provision_public.html)。

对于 {{site.data.keyword.cloud_notm}} 目录，您必须具有升级的帐户才能订购虚拟服务器。有关升级帐户的更多信息，请参阅[切换到 IBM 标识](https://console.bluemix.net/docs/admin/softlayerlink.html)。
{:note}

### 通过 Softlayer API 供应
您可以通过 {{site.data.keyword.slapi_short}} 来供应支持暂挂计费功能的虚拟服务器实例。对于 API 示例，请参阅[使用下单对象供应公共实例](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object)。 

在供应过程中，必须指定特定暂挂计费软件包标识。您可以在 {{site.data.keyword.slapi_short}} 中使用密钥名 `SUSPEND_CLOUD_SERVER` 查询暂挂计费软件包标识。有关搜索服务器软件包的示例，请参阅[通过使用 {{site.data.keyword.slapi_short}} 订单 CLI 了解和构建订单 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/article/understanding-ordering/){: new_window}。

## 计费详细信息

请务必了解在虚拟服务器实例关闭时哪些成本停止增加，哪些成本持续存在。

| 资源                      | 计费停止   | 计费持续 |
| ----------------------------- | ----------------- | ---------------- |
|vCPU|X|                  |
|RAM|X|                  |
|端口速度|X|                  |
|操作系统许可证            |X|                  |
| 监视附加组件            |X|                  |
| 辅助公共 IP 地址         |                   |X|
|存储器|                   |X|
{: caption="表 1. 资源计费详细信息" caption-side="top"}   

供应支持暂挂计费功能的虚拟服务器实例时，对于虚拟服务器实例的使用中时间和暂挂时间，将每分钟计算使用时间。即使您关闭了实例，从而从不启动暂挂计费功能，也将在实例生命周期内每分钟计算计费。
{:note}

### 最低使用量费用
在某些情况下，支持暂挂计费功能的虚拟服务器实例可能适用每个月有最低使用量费用。如果使用量大于 25%，将根据该使用量向您计费。如果使用量小于 25%，将根据实例在当前计费周期中存在的小时数的 25% 收费。 

### 计费发票
暂挂虚拟服务器上的计费时，您将看到计费发票中的一些变化。相关费用现在显示为基于使用量的详细信息。例如，您可能看到反映可用小时数、已用小时数和收费小时总数的以下新增项：

```
Computing instance usage...
RAM usage...
Operating system usage...
```
{:screen}

## 资源详细信息

### 存储器

在虚拟服务器实例上暂挂计费时，对关联的存储器持续计费，但是您在虚拟服务器实例关闭的情况下无法访问存储的数据。恢复对实例的计费后，您可以再次访问数据。

### IP 地址

对虚拟服务器实例暂挂计费时，将为您保留所有公共 IP 地址。

### 限制

暂挂的虚拟服务器实例仍将计入整个帐户的设备配额中。有关实例限制的更多信息，请参阅[常见问题：虚拟服务器](vsi_faqs_vs.html#concurrent)。

## 后续步骤
供应支持暂挂计费的虚拟服务器后，您可以开始暂挂和恢复设备上的计费。


在虚拟服务器实例上暂挂计费时，您在恢复设备的计费之前，无法在实例上完成所有相同操作。您可以通过 {{site.data.keyword.slapi_short}} 或访问 {{site.data.keyword.slportal}} 中的“设备详细信息”页面，以查看您的设备是否已停止，以及状态更改时的相关日期。

要暂挂虚拟服务器实例上的计费，请关闭虚拟服务器。有关更多信息，请参阅[管理虚拟服务器](vsi_managing.html)。
