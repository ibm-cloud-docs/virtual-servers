---



copyright:
  years: 2017, 2018
lastupdated: "2018-10-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 供应公共实例
{: #ordering-vs-public}

## 开始之前
有两个选项可供应公共虚拟服务器实例。第一个是通过 {{site.data.keyword.Bluemix}} 目录，第二个是通过 {{site.data.keyword.slportal}}。目录和 {{site.data.keyword.slportal}}需要唯一登录标识。目录的用户名和密码无法用于登录到门户网站，反之亦然。
{:shortdesc}

开始之前，请查看以下先决条件。

  1. 确保您已设置 {{site.data.keyword.Bluemix_notm}} 目录或 {{site.data.keyword.slportal}}凭证。

     **注**：对于 {{site.data.keyword.Bluemix_notm}} 目录，您必须具有升级的帐户才能订购虚拟服务器。有关升级帐户的更多信息，请参阅[切换到 IBM 标识](https://console.bluemix.net/docs/admin/softlayerlink.html)。

  2. 如果尚未查看可供您使用的部署选项，请执行此操作。有关更多信息，请参阅[部署选项：公共虚拟服务器](../vsi/vsi_public.html)。

  3. 复查虚拟服务器实例容量注意事项。有关更多信息，请参阅[容量注意事项](ts_capacity_bp.html)。

## 供应公共虚拟服务器实例
{: #ordering-public-instance}

完成先决条件后，可以开始供应公共虚拟服务器实例。可以通过 {{site.data.keyword.cloud_notm}} 目录或 {{site.data.keyword.slportal}} 来供应公共实例。

### 通过 IBM Cloud 目录供应公共虚拟服务器实例
要通过 {{site.data.keyword.cloud_notm}} 目录来供应公共虚拟服务器实例，请完成以下步骤：

  1. 使用您的唯一凭证来登录到 [{{site.data.keyword.cloud_notm}} 目录 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/catalog/){: new_window}。 
  2. 在**计算基础架构**部分中，单击**虚拟服务器**磁贴。
  3. 选择**公共虚拟服务器**选项。
  4. 单击**创建**。
  5. 填写虚拟服务器实例的所有相关信息。 
  6. 复查订单摘要后，单击**第三方服务协议**复选框。 
  7. 单击**供应**。
  
### 通过客户门户网站供应公共虚拟服务器实例
要通过 {{site.data.keyword.slportal}} 来供应公共虚拟服务器实例，请完成以下步骤：

  1. 使用您的唯一凭证来登录到 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。
  2. 找到**订购**部分，然后单击**设备**。 
  3. 在“设备”页面上，对其中一个虚拟服务器产品，单击**每小时 SAN**、**每小时本地**、**每月**或**瞬态**。
  4. 在*配置云服务器*页面上，填写所有相关信息。
  5. 单击**添加到订单**按钮以继续。
  6. 确认或编辑服务器的域信息。
  7. 单击**云服务条款**和**第三方服务协议**复选框。
  8. 确认或输入付款信息，然后单击**提交订单**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

 将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于在您登录到 {{site.data.keyword.Bluemix_notm}} 后转至*设备详细信息*页面。您还可以直接登录到 {{site.data.keyword.slportal}}。

## 后续步骤
供应虚拟服务器后，即可以开始对其进行管理。有关更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。
