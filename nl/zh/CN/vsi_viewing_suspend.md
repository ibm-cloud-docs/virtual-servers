---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 查看暂挂计费功能
{: #viewing-suspend-billing-feature}

## 开始之前
首先，导航至设备菜单，并确保您具有完成任务的正确帐户许可权。 

* 导航至控制台的设备菜单。有关更多信息，请参阅[导航至设备](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 确保您具有任何必需的帐户许可权和设备访问权。只有帐户所有者或具有**管理用户**经典基础架构许可权的用户才能调整许可权。 

有关许可权的更多信息，请参阅[经典基础架构许可权](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理设备访问权](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 查看暂挂计费功能 
要确定虚拟服务器实例是否支持暂挂计费功能，请执行下列步骤：

1. 在**设备**菜单中，选择**设备列表**。 
2. 在**设备列表**中，单击虚拟服务器实例的名称。 
3. 在**实例详细信息**部分中，您可以查看虚拟服务器实例是否支持暂挂计费功能。 

|字段|值|
| --------------------------------------| ------------------------- |
| 暂挂计费：在关闭电源时启用 | 支持该功能。     |
| 暂挂计费：不可用          | 不支持该功能。     |
{: caption="表 1. 暂挂计费详细信息" caption-side="top"}

## 通过 SoftLayer API 查看暂挂计费功能

以下命令是在 {{site.data.keyword.slapi_short}} 中请求验证虚拟服务器实例是否支持暂挂计费功能的示例。

以下 JSON 请求和响应为通用示例。
{:note}

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
1. [暂挂计费](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [管理虚拟服务器](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

