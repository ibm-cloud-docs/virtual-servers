---

copyright:
  years: 2018, 2019
lastupdated: "2019-03-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 查看暂挂计费功能
{: #viewing-suspend-billing-feature}

您可以在 {{site.data.keyword.slportal_full}} 中或通过 {{site.data.keyword.slapi_short}} 来查看自己的虚拟服务器实例是否支持暂挂计费功能。

## 在客户门户网站中查看暂挂计费功能
要在 {{site.data.keyword.slportal}} 中确定虚拟服务器实例是否支持暂挂计费功能，请执行下列步骤：

1. 使用您的唯一凭证来登录到 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。
2. 在**设备**菜单中，选择**设备列表**。
3. 在**设备列表**中，单击虚拟服务器实例的名称。
4. 在**配置**选项卡的**常规**部分，可以查看虚拟服务器实例是否支持暂挂计费功能。

|字段|值|
| --------------------------------------| ------------------------- |
| 暂挂计费：在关闭电源时启用 | 支持该功能。     |
| 暂挂计费：不可用 | 不支持该功能。     |
{: caption="表 1. 暂挂计费详细信息" caption-side="top"}

## 通过 Softlayer API 查看暂挂计费功能

以下命令是在 {{site.data.keyword.slapi_short}} 中请求验证虚拟服务器实例是否支持暂挂计费功能的示例。

**注**：以下 JSON 请求和响应是通用示例。

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

下面是该请求的 JSON 响应示例：

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

有关更多信息，请参阅[SLDN API 文档 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}。

## 后续步骤

要了解有关暂挂计费功能的更多内容，请查阅以下信息：
1. [关于暂挂计费](/docs/vsi?topic=virtual-servers-requirements)
2. [管理虚拟服务器](/docs/vsi?topic=virtual-servers-managing-virtual-servers)
