---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# 常见问题：虚拟服务器  
{: #faqs-virtual-servers}

## 哪些类型的虚拟服务器可供使用？
{: faq}
{{site.data.keyword.BluSoftlayer_full}} 在其经典基础架构中提供了几种类型的虚拟服务器。标准产品是基于公共的虚拟服务器，这是适合各种需求的多租户环境。如果寻找的是单租户环境，请考虑使用“专用虚拟服务器”产品。专用虚拟服务器选项非常适合资源需求更严格的应用程序。有关当前虚拟服务器产品的更多信息，请参阅[虚拟服务器入门](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers)。

IBM Cloud 提供了虚拟私有云 (VPC) 基础架构，这是下一代云平台。您可以在 {{site.data.keyword.cloud_notm}} 中创建自己的空间，以通过使用 VPC 在公共云中运行隔离环境。VPC 提供了私有云的安全性以及公共云的敏捷性和易用性。有关更多信息，请参阅[关于虚拟私有云](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about)。

## 在哪里可以找到公共实例类型的定价信息？
{: faq}

有关定价信息，请参阅[构建虚拟服务器 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/cloud/virtual-servers){: new_window}。

## 在哪里可以找到虚拟公共实例的定价信息？
{: faq}

估算 {{site.data.keyword.cloud_notm}} 服务器支持工作负载的成本从 [{{site.data.keyword.cloud_notm}} 目录](https://cloud.ibm.com/catalog)开始。从目录中，选择**计算**并选择服务器类型 - 裸机服务器、虚拟服务器或适用于 VPC（虚拟私有云）的虚拟服务器。有关定价信息，请参阅 [Virtual servers provisioning calculator ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}。

## 可以向每小时或每月虚拟服务器添加磁盘存储吗？
{: faq}

通过在要更新的设备的*配置*屏幕中，更新*第一个磁盘*到*第五个磁盘*字段中的存储选项，可以升级或降级任何虚拟服务器的磁盘存储。有关更多信息，请参阅[重新配置现有虚拟服务器](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers)。

## 可以启动多少个每小时虚拟服务器？
{: #concurrent}
{: faq}

您可以运行的实例数取决于帐户的成熟度级别。缺省情况下，在任意时间，超过 45 天的帐户可以在公共虚拟服务器、专用虚拟服务器和裸机服务器上运行的实例数限制为 20。帐户越新，实例数限制越小。如果要提高此限制，请联系支持人员，为我们多提供一些有关您要执行的操作以及可能需要的并发实例数的信息。

## 对于每小时虚拟服务器的带宽，会如何计费？
{: faq}

每小时虚拟计费分解为入站和出站流量。虚拟服务器的所有入站流量都是免费的。出站流量按 GB 计量和收费，在结算周期结束时会评估总量。

## 在什么情况下，虚拟服务器会迁移到其他主机？
{: faq}

在有限的情况下，可能需要将虚拟服务器迁移到其他主机。如果需要迁移，那么会关闭、迁移并重新启动虚拟服务器。在以下情况下，可能会迁移虚拟服务器：

* 需要更新系统管理程序，正在解除主机，或不允许主机执行新实例。如果某个主机标记为要进行其中任一更改，那么在 {{site.data.keyword.cloud_notm}} 控制台中重新引导该主机的某个虚拟服务器时，重新引导会自动触发将该虚拟服务器迁移到其他主机。
* 基础架构维护。您可能会收到一封电子邮件，指明托管虚拟服务器的系统上需要维护。在基础架构维护过程中，可能需要迁移您的虚拟服务器。
* 升级到现有实例。为了获得一致的性能，如果升级实例，可能会将其迁移到其他主机，以确保该实例收到合适的专用 CPU 和内存。
* 某个专用主机发生故障。专用实例将迁移到另一个空主机，而不使用您可能具有的任何现有容量。

在维护时段内，您可能会看到在 {{site.data.keyword.cloud_notm}} 控制台中设备的**操作**菜单中显示有**迁移主机**选项。通过**迁移主机**，可以在指定的维护时间段内您方便的时候将虚拟服务器迁移到新主机。如果在维护时间段内未启动迁移，那么将自动迁移虚拟服务器以完成必需的维护。**迁移主机**选项不会持久存在，仅在通过维护通知传达的维护时间段内可用。

如果某个虚拟服务器需要具有的特定级别系统管理程序在当前主机上不可用，那么也可能会看到**迁移主机**选项。

## 删除可移植存储器时，数据会发生什么情况？
{: faq}

删除存储器时，会除去指向该卷上数据的所有指针，因此数据会变得无法访问。如果将该物理存储器重新供应到其他帐户，那么会分配一组新的指针。新帐户无法访问物理存储器上可能存在的任何数据。新的一组指针会显示为全是 0。将新数据写入卷/LUN 时，会覆盖仍然存在的任何不可访问的数据。

## 可以使用 Red Hat Cloud Access 预订来创建虚拟服务器吗？
{: faq}

可以。导入映像时，可以指定您将提供操作系统许可证。有关更多信息，请参阅[使用 Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription)。然后，可以通过该映像模板订购虚拟服务器，并使用现有的 [Red Hat Cloud Access ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} 预订。

## 虚拟服务器与虚拟专用服务器 (VPS) 有什么区别？
{: faq}

虚拟服务器类似于您可能已经很熟悉的虚拟专用服务器 (VPS) 或虚拟专用服务器 (VDS) 平台。这些“虚拟服务器”环境支持在单个硬件节点上以专用、安全的方式供应不同的环境，但 VDS 和 VPS 在功能方面有更多限制。VPS 和 VDS 选项通常仅限于单服务器体系结构。可以在 VDS 或 VPS 上的每个虚拟服务器之间添加或划分的唯一资源是物理安装在该单个服务器上的资源。

虚拟服务器是在多服务器云体系结构上供应的，该体系结构将所有可用硬件资源合并在一起供各个实例使用。虚拟服务器可以使用基于 SAN 的共享高容量主存储平台或高性能本地磁盘存储。由于每个实例都是更大的云环境的一部分，因此所有虚拟服务器之间的通信都是即时的。

## 为什么我在供应虚拟服务器时收到容量错误？
{: faq}

供应虚拟服务器时，您可能会收到错误消息，说容量不足，无法完成请求。供应失败时，该特定请求中的所有虚拟服务器实例均会失败。
路由器或数据中心的可用资源不足而无法执行服务请求时，会发生容量错误。有多个原因可能会导致您收到此错误。资源可用性变化频繁，因此您可以等待并稍后重试。有关避免此错误的策略的更多信息，请参阅[虚拟服务器实例的资源注意事项](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations)。

## 如何登录到我的服务器？
{: faq}

登录到控制台并导航至**设备**菜单。有关更多信息，请参阅[导航至设备](/docs/vsi?topic=virtual-servers-navigating-devices)。在**设备列表**中，选择您的实例。您可以查看和管理用于登录的设备用户名和密码。有关更多信息，请参阅[查看和管理设备用户名和密码](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device)。 

## 如何使用 VPN 来访问 IBM Cloud 专用网络？
{: faq}

您可以通过 [Web 界面](https://www.softlayer.com/VPN-Access){: external}或使用适用于 Linux、macOS 或 Windows 的[单机 VPN 客户端](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients)登录到 VPN。有关连接到 VPN 后要执行的操作的更多信息，请参阅[使用 SSL VPN](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn)。

## 如何重新引导虚拟服务器？
{: faq}

设备重新引导可以通过**设备列表**或单个设备的“快照”视图来执行。在控制台的**设备列表**中导航至虚拟服务器实例。有关更多信息，请参阅[导航至设备](/docs/vsi?topic=virtual-servers-navigating-devices)。针对要管理的设备，选择**操作**，然后选择**重新引导**。

## 如何使用急救内核？
{: faq}

如果您遇到服务器问题，那么引导至急救内核会很有帮助。要启动急救内核，请从控制台中的**设备列表**中选择设备名称。在**操作**菜单中，选择**急救方式**或为 Windows 实例选择**从映像引导**。有关更多信息，请参阅[启动急救内核](/docs/vsi?topic=virtual-servers-launching-rescue)。

## 在哪里可以找到网络状态？
{: faq}

您可以直接在 [{{site.data.keyword.cloud_notm}} - 状态](https://cloud.ibm.com/status){: external}处访问**状态**页面，以查看所有 {{site.data.keyword.cloud_notm}} 位置中资源的当前状态。您可以通过选择特定组件和位置来过滤列表（例如，可以选择“虚拟服务器”并查看网络连接）。

## 如何请求一致性报告？
{: faq}

有关查看或请求一致性信息（包括 SOC 报告）的信息，请参阅[如何知道我的数据是安全的？](/docs/overview?topic=overview-security)

