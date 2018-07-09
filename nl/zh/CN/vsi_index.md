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
{:table: .aria-labeledby="caption"}

# 虚拟服务器入门
您可以在几分钟内部署 {{site.data.keyword.BluVirtServers}}。虚拟服务器将基于您选择的虚拟服务器映像，部署在适合使用工作负载的地理区域中。
{:shortdesc}

创建虚拟服务器时，可以选择是公共（多租户）环境还是专用（单租户）环境。然后，根据所选环境，还必须选择每小时、每月或瞬态虚拟服务器。对于公共虚拟服务器，还可选择是使用基于 SAN 的存储器还是本地存储器。

## 开始之前

开始之前，请查看以下先决条件。

  1. 您必须具有升级的帐户才能订购虚拟服务器。此过程可能需要一些时间，并且需要先核准您的请求后才能继续。有关升级帐户的更多信息，请参阅[切换到 IBM 标识](https://console.bluemix.net/docs/admin/softlayerlink.html)。
  2. 查看并选择部署选项。有关更多信息，请参阅以下主题：

|部署选项|描述|
| --------------------------------------------------------- | --------------------------------------------------- |
|[公共虚拟服务器](../vsi/vsi_public.html)|IBM 管理的多租户虚拟服务器部署|
|[瞬态虚拟服务器](../vsi/vsi_about_transient.html)|以更低成本提供 IBM 管理的多租户虚拟服务器部署，最适用于灵活的工作负载|
|[专用虚拟服务器](../vsi/vsi_dedicated.html)|IBM 管理的单租户虚拟服务器部署|
{: caption="表 1. 部署选项" caption-side="top"}   

## 供应虚拟服务器

在您决定部署选项后，开始供应过程。

|供应指示信息|描述|
| -------------------------------------------------------------------------- | ------------------------------------------------------- |
|[供应公共实例](../vsi/vsi_provision_public.html)|使用各种选项来供应公共实例|
|[供应瞬态实例](../vsi/vsi_provision_transient.html)|使用各种选项来供应瞬态实例|
|[供应专用主机和实例](../vsi/vsi_provision_dedicated.html)|在专用主机上供应私有实例或专用实例。|
{: caption="表 2. 供应信息" caption-side="top"}

## 后续步骤

虚拟服务器已供应并可供使用后，可以使用 {{site.data.keyword.slportal_full}}或 {{site.data.keyword.slapi_full}} 来配置虚拟服务器。有关更多信息，请参阅[配置虚拟服务器](../vsi/vsi_configuring.html)。
