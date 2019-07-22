---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# 关于专用虚拟服务器
{: #dedicated-virtual-servers}

{{site.data.keyword.Bluemix}} Infrastructure 专用主机产品是一种虚拟化的单租户专用服务器。您可借此最大程度地控制工作负载布置，并使用灵活的供应后选项。您可以决定将虚拟服务器布置在哪个预先确定的 {{site.data.keyword.cloud_notm}} 中，并可以通过将主机直接分配给您的帐户来确保容量。
{:shortdesc}

此产品包含以下功能：

* 亲缘关系和反亲缘关系。可以指定应保留的主机到虚拟服务器关系和虚拟服务器到虚拟服务器关系，这些称为亲缘关系和反亲缘关系规则。这些规则可帮助您确保根据工作负载需求来相应地布置工作负载。
* 部署后管理。可以根据工作负载需求在专用主机之间迁移虚拟服务器。
* 工作负载可视性。可以查看每个主机的资源耗用情况（核心、RAM 和本地存储器），从而最大程度地控制工作负载管理。

您有两种部署模型可供选择：专用主机和专用实例。专用主机帮助控制工作负载布置，而专用实例提供单租户隔离。

专用主机提供的某些控制功能在专用实例中并未提供。有关更多详细信息，请参阅下表。
{:note}

|专用虚拟服务器功能|专用主机实例|专用实例|
| ------- | ------- | ------- |
|单租户隔离| ![复选标记图标](../../icons/checkmark-icon.svg) | ![复选标记图标](../../icons/checkmark-icon.svg) |
|虚拟服务器布置控制| ![复选标记图标](../../icons/checkmark-icon.svg) |   |
|资源可视性| ![复选标记图标](../../icons/checkmark-icon.svg) |   |
|实例计费|   | ![复选标记图标](../../icons/checkmark-icon.svg) |
| 主机计费<sup>(1)</sup> | ![复选标记图标](../../icons/checkmark-icon.svg) |   |
|部署后控制| ![复选标记图标](../../icons/checkmark-icon.svg) |   |
|容量保留| ![复选标记图标](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="表 1. 控制功能" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup>主机定价包含核心、RAM、本地 SSD 和网络速度在内。高级操作系统 (OS)、存储区域网络 (SAN) 存储器和软件附加组件将根据每小时或每月模型中的现有定价和许可按实例定价。

订购专用主机和专用主机实例时，请记住以下各点：

* 主机的大小根据您将运行的工作负载来确定。缺省值为 56 核心 X 242 GB RAM X1.2 TB，但您可以从其他配置中进行选择。
* 一次只能订购 2 个主机。例如，如果需要 6 个主机，您将需要下 3 个单独的订单。
* 每个主机都将需要自己的唯一名称，并且您可以自动分配 POD。

## 后续步骤

复查并决定了部署选项之后，即可以供应虚拟服务器。要开始操作，请参阅[供应专用主机和实例](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated)。
