---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-26"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 关于暂挂计费 (Beta)
{: #requirements}

关闭支持暂挂计费功能的虚拟服务器时，您不会增加特定计算资源的成本。服务器关闭后会自动停止计费。暂挂计费功能可帮助您降低成本，并使您在再次需要资源时不必重新供应虚拟服务器。仅支持对新供应暂挂计费，而不是现有实例。
{:shortdesc}

要访问暂挂计费功能，您必须使用 {{site.data.keyword.slapi_short}} 供应新的虚拟服务器实例，以指定暂挂计费软件包。新的虚拟服务器实例必须使用以下设置进行配置：

* 每小时 SAN
* 以下某一个系列：
  * 均衡
  * 计算
  * 内存
* 以下某一个 {{site.data.keyword.cloud}} 数据中心：

|数据中心|         |
| ------------ | ------- | 
|SEO01  |WDC01   |
|SAO01  |WDC04  |
|TOK02  |WDC06  |
|DAL01        |WDC07  |
|DAL05         |LON02         |
|DAL06         |LON04         |
|DAL09         |LON06   |
|DAL10         |FRA02         |
|DAL12         |  FRA04  |
|DAL13         |  FRA05  |
{: caption="表 1. 支持的数据中心" caption-side="top"}

您可以使用暂挂计费功能，作为供应和取消供应虚拟服务器实例的更快替代方法。
{:tip}

## 供应

对于 beta，要供应支持暂挂计费功能的虚拟服务器实例，您必须使用 {{site.data.keyword.slapi_short}}。对于 API 示例，请参阅[使用下单对象供应公共实例](../vsi/vsi_provision_api.html#provisioning-a-public-instance-using-place-order-object)。 

您还必须在供应过程中指定特定暂挂计费软件包标识。您可以在 {{site.data.keyword.slapi_short}} 中使用密钥名 `SUSPEND_CLOUD_SERVER` 查询暂挂计费软件包标识。有关搜索服务器软件包的示例，请参阅[通过使用 {{site.data.keyword.slapi_short}} 订单 CLI 了解和构建订单 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/article/understanding-ordering/){: new_window}。

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

**注：**供应支持暂挂计费功能的虚拟服务器实例时，对于虚拟服务器实例的使用中时间和暂挂时间，将每分钟计算使用时间。即使您关闭了实例，从而从不启动暂挂计费功能，也将在实例生命周期内每分钟计算计费。 

### 最低使用量费用
支持暂挂计费功能的虚拟服务器实例每个月有最低使用量费用。如果使用量大于 25%，将根据该使用量向您计费。如果使用量小于 25%，将根据实例在当前计费周期中存在的小时数的 25% 收费。 

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

暂挂虚拟服务器实例上的计费时，关联的存储器持续存在，但是您在虚拟服务器实例关闭的情况下无法访问数据。恢复对实例的计费后，您可以访问数据，然后将再次开始正常计费。

### IP 地址

对虚拟服务器实例暂挂计费时，将为您保留所有公共 IP 地址。

您可以通过 {{site.data.keyword.slapi_short}} 或访问 {{site.data.keyword.slportal_full}} 中的“设备详细信息”页面，以查看您的设备是否已停止，以及状态更改时的相关日期。

### 限制

支持的并发实例数是您的帐户内设备配额的一部分。有关并发实例限制的更多信息，请参阅[常见问题：虚拟服务器](vsi_faqs_vs.html#concurrent)。

## 后续步骤
供应支持暂挂计费的虚拟服务器后，您可以开始暂挂和恢复设备上的计费。
暂挂虚拟服务器实例上的计费时，您在恢复设备的计费之前，无法在实例上完成所有相同操作。

要暂挂虚拟服务器实例上的计费，请关闭虚拟服务器。有关更多信息，请参阅[管理虚拟服务器](vsi_managing.html)。
