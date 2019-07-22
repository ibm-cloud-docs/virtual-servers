---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# 从第三方映像供应虚拟服务器实例
{: #ordering-3P}

您可以从第三方供应商创建的映像供应虚拟服务器实例。通过 {{site.data.keyword.cloud}} 目录“云映像”链接提供了第三方映像。
{:shortdesc}

## 开始之前
开始之前，请确保已设置 {{site.data.keyword.cloud_notm}} 目录凭证。

对于 {{site.data.keyword.Bluemix_notm}} 目录，您必须具有升级的帐户才能订购虚拟服务器。有关升级帐户的更多信息，请参阅[切换到 IBM 标识](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)。
{:note}

## 选择虚拟服务器映像
1. 使用您的唯一凭证来登录到 [{{site.data.keyword.cloud_notm}} 目录 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/catalog/){: new_window}。
2. 在**云映像**部分中，找到并单击要部署的第三方映像。
3. 查看定制图像详细信息，然后单击**继续**。将显示**虚拟服务器实例 - 定制映像**页面，并且会预先选择您的定制映像。

## 复查和选择部署选项
有关更多信息，请参阅以下主题：

|部署选项|描述|
| --------------------------------------------------------- | --------------------------------------------------- |
|[公共虚拟服务器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)|IBM 管理的多租户虚拟服务器部署|
|[瞬态虚拟服务器](/docs/vsi?topic=virtual-servers-transient-virtual-servers#transient-virtual-servers)|以更低成本提供 IBM 管理的多租户虚拟服务器部署，最适用于灵活的工作负载|
|[预留虚拟服务器](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers#about-reserved-virtual-servers)|IBM 管理的多租户虚拟服务器部署，在合同期内提供保证的容量|
|[专用虚拟服务器](/docs/vsi?topic=virtual-servers-about-dedicated-virtual-servers#about-dedicated-virtual-servers)|IBM 管理的单租户虚拟服务器部署|
{: caption="表 1. 部署选项" caption-side="top"}

## 供应虚拟服务器
在您决定部署选项后，开始供应过程。有关更多信息，请参阅以下主题。

由于是使用定制映像启动供应过程的，因此无法在供应过程期间更改映像类型。
{:note}

|              供应指示信息                                         |描述|
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[供应公共实例](/docs/vsi?topic=virtual-servers-ordering-vs-public#ordering-vs-public)|使用各种选项来供应公共实例|
|[供应瞬态实例](/docs/vsi?topic=virtual-servers-ordering-vs-transient#ordering-vs-transient)|使用各种选项来供应瞬态实例|
|[供应预留容量和实例](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)|使用各种选项来供应预留容量和实例|
|[供应专用主机和实例](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated#ordering-vs-dedicated)|在专用主机上供应私有实例或专用实例。|
{: caption="表 2. 供应信息" caption-side="top"}


## 后续步骤
虚拟服务器已供应并可供使用后，可以使用 {{site.data.keyword.cloud_notm}} 控制台或 {{site.data.keyword.slapi_short}} 来配置虚拟服务器。有关更多信息，请参阅[配置虚拟服务器](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)。
