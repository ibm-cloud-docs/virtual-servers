---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 供应瞬态实例
{: #ordering-vs-transient}
可以通过 {{site.data.keyword.slportal_full}}来供应瞬态虚拟服务器实例。
{:shortdesc}

## 开始之前
开始之前，请查看以下先决条件。

  1. 确保已设置 {{site.data.keyword.slportal}}凭证。

  2. 复查虚拟服务器实例容量注意事项。有关更多信息，请参阅[容量注意事项](ts_capacity_bp.html)。

## 登录
确保您已登录到 {{site.data.keyword.slportal}}：

  1. 使用您的唯一凭证来访问 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。

这将打开 {{site.data.keyword.slportal}}的主页。

## 供应瞬态虚拟服务器实例
{: #ordering-transient-instance}
完成先决条件后，供应瞬态虚拟服务器实例。您可以通过两种方法（通过**设备**菜单或**设备**图标）来供应瞬态实例。

### 通过设备图标供应瞬态虚拟服务器实例
要通过*设备*图标来供应瞬态虚拟服务器实例，请完成以下步骤：

1.  在 {{site.data.keyword.slportal}}中，找到**订购**部分，然后单击**设备**。
2.  在*设备*页面上的*公共虚拟服务器*下，对虚拟服务器产品，单击**瞬态**。
3.  在*配置云服务器*页面上，填写所有相关信息。
4.  单击**添加到订单**以继续。
5.  确认或编辑服务器的域信息。
5.  单击**云服务条款**和**第三方服务协议**复选框。
6.  确认或输入付款信息，然后单击**提交订单**。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

 将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于供您转至*设备详细信息*页面。

### 通过设备菜单供应瞬态虚拟服务器实例
{: #ordering-transient-devices-menu}

您还可以通过 {{site.data.keyword.slportal}}主页上的*设备*菜单来供应瞬态虚拟服务器实例。

1. 单击**设备 > 设备列表**。

   “设备”页面将显示您帐户中的所有设备类型：专用主机、虚拟服务器、裸机服务器和 NetScaler 应用程序交付控制器。
2. 单击右上角的**订购设备**链接。
3. 在*设备*页面上的*公共虚拟服务器*下，对虚拟服务器产品，单击**瞬态**。
4. 在*配置云服务器*页面上，填写所有相关信息。
5. 单击**添加到订单**以继续。
6. 确认或编辑服务器的域信息。
7. 单击**云服务条款**和**第三方服务协议**复选框。
8. 确认或输入付款信息，然后单击**提交订单**。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于供您转至*设备详细信息*页面。

您还可以使用 {{site.data.keyword.slapi_short}}来供应瞬态虚拟服务器。有关示例，请参阅[使用创建对象供应瞬态实例](../vsi/vsi_provision_api.html#api-rest-transient)。
{:tip}

## 后续步骤
供应虚拟服务器后，即可以开始对其进行管理。有关更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。
