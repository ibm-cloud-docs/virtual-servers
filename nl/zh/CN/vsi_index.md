---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-29"

keywords: virtual servers, provisioning process, IBM Cloud Virtual Servers

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 入门教程
{: #getting-started-tutorial}

您可以在几分钟内部署 {{site.data.keyword.BluVirtServers}}。虚拟服务器将基于您选择的虚拟服务器映像，部署在适合使用工作负载的地理区域中。
{:shortdesc}

请在虚拟私有云上试用虚拟服务器！有关更多信息，请参阅 [IBM Cloud Virtual Server for Virtual Private Cloud](/docs/vpc-on-classic-vsi?topic=vpc-on-classic-vsi-getting-started)。
{:tip}

在经典基础架构中创建虚拟服务器时，可以选择是公共（多租户）环境还是专用（单租户）环境。然后，根据所选环境，还必须选择每小时、每月或瞬态虚拟服务器。对于公共虚拟服务器，还可选择是使用基于 SAN 的存储器还是本地存储器。

## 开始之前

开始之前，请查看以下先决条件。

  1. 您必须具有升级的帐户才能订购虚拟服务器。此过程可能需要一些时间，并且需要先核准您的请求后才能继续。有关升级帐户的更多信息，请参阅[切换到 IBM 标识](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)。
  2. 查看并选择部署选项。有关更多信息，请参阅以下主题：

|部署选项|描述|
| --------------------------------------------------------- | --------------------------------------------------- |
|[公共虚拟服务器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)|IBM 管理的多租户虚拟服务器部署|
|[瞬态虚拟服务器](/docs/vsi?topic=virtual-servers-about-vs-transient)|以更低成本提供 IBM 管理的多租户虚拟服务器部署，最适用于灵活的工作负载|
|[预留虚拟服务器](/docs/vsi?topic=virtual-servers-about-reserved-virtual-servers)|IBM 管理的多租户虚拟服务器部署，在合同期内提供保证的容量|
|[专用虚拟服务器](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)|IBM 管理的单租户虚拟服务器部署|
{: caption="表 1. 部署选项" caption-side="top"}   

## 供应虚拟服务器

在您决定部署选项后，开始供应过程。

|              供应指示信息                                         |描述|
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[供应公共实例](/docs/vsi?topic=virtual-servers-ordering-vs-public)|使用各种选项来供应公共实例|
|[供应瞬态实例](/docs/vsi?topic=virtual-servers-ordering-vs-transient)|使用各种选项来供应瞬态实例|
|[供应预留容量和实例](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances)|使用各种选项来供应预留容量和实例|
|[供应专用主机和实例](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)|在专用主机上供应私有实例或专用实例。|
{: caption="表 2. 供应信息" caption-side="top"}

## 后续步骤

虚拟服务器已供应并可供使用后，可以使用 {{site.data.keyword.cloud_notm}} 控制台或 {{site.data.keyword.slapi_short}} 来配置虚拟服务器。有关更多信息，请参阅[配置虚拟服务器](/docs/vsi?topic=virtual-servers-configuring-virtual-servers)。
