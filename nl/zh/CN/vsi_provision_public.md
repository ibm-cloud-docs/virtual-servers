---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-17"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 供应公共实例
{: #ordering-vs-public}

## 开始之前
有两个选项可供应公共虚拟服务器实例。第一个是通过 {{site.data.keyword.cloud}} 控制台，第二个是通过 {{site.data.keyword.slportal}}。控制台和 {{site.data.keyword.slportal}} 需要唯一登录标识。您无法使用控制台的用户名和密码登录门户网站，反之亦然。
{:shortdesc}

对于 {{site.data.keyword.cloud_notm}} 控制台，您必须具有升级的帐户才能订购虚拟服务器。有关升级帐户的更多信息，请参阅[现收现付帐户](/docs/account?topic=account-accounts#paygo)。
{:note}

开始之前，请查看以下先决条件。

  1. 查看可供您使用的部署选项。有关更多信息，请参阅[公共虚拟服务器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers#about-public-virtual-servers)。

  2. 复查虚拟服务器实例容量注意事项。有关更多信息，请参阅[虚拟服务器实例的资源注意事项](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations)。
  
  3. 从 {{site.data.keyword.cloud_notm}} 控制台打开[虚拟服务器实例 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} 页面。

## 供应公共虚拟服务器实例  
{: #ordering-public-instance}

要供应虚拟服务器实例，您需要考虑以下信息。

您必须登录才能查看所有可用选项。
{:tip}

### 公共实例

|字段|详细信息|
| -------- | ----------- |
|计费|根据虚拟服务器实例，可以选择每小时或每月计费。除了成本外，主要的差异在于每小时实例没有包含带宽分配量。在计费周期结束时，将计算帐户上每个实例的带宽使用量和处于活动状态的小时数。例如，如果您在 10 天后取消每小时实例，那么只需支付这 10 天的小时数。如果您在 10 天后取消每月实例，那么将支付整个月的费用。如果您对暂挂计费功能（仅在每小时实例中可用）感兴趣，请参阅[关于暂挂计费](/docs/vsi?topic=virtual-servers-about-suspend-billing)。|
|主机名|可以包含多个由字母数字字符和短划线组成的标签，并以句点分隔。标签不能只包含数字，不能以短划线开头或结尾，也不能包含连续的短划线或句点。|
|域|必须包含两个或多个可以由字母数字字符和短划线组成的标签，并以句点分隔。标签不能以短划线开头或结尾，也不能包含连续的短划线或句点。最后一个标签必须仅使用字母。|
|放置组|您可以为实例选择放置组。如果添加放置组，那么“传播”规则表示各个实例在不同的物理硬件上。有关更多信息，请参阅[放置组](/docs/vsi?topic=virtual-servers-placement-groups)。|
|位置|位置由区域（特定地理区域）和专区（区域内的容错数据中心）组成。选择要在其中创建虚拟服务器实例的位置。 |
|常用概要文件| 请考虑从支持最常见用例的常用概要文件配置中进行选择。概要文件包含在几分钟内即可供使用的预配置实例。|
|所有概要文件|有关公共实例的可用概要文件选项的更多信息，请参阅[公共虚拟服务器](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)。|
|SSH 密钥|利用 SSH 密钥，无需使用密码即可从在实例上实现的每个公用密钥所对应的客户机来访问实例。如果您决定添加 SSH 密钥，请提供 SSH 密钥的公用密钥，您可以使用该密钥在供应实例后登录到实例。|
| 映像        |  映像是实例的已部署操作系统。您有若干免费选项可选择，例如 CentOS 和 Ubuntu。另外，还提供了付费选项，例如 Windows Server 和 Red Hat EnterpriseLinux (RHEL)。值得注意的是 Windows 需要一个 100 GB 的主磁盘。|
{: caption="表 1. 公共实例选项" caption-side="top"}

### 公共实例附加组件 

如果选择任何操作系统、控制面板或软件附加组件，那么它们必须与您的映像兼容，以避免在订购实例时发生错误。例如，不能使用 Microsoft 数据库供应 RedHat 映像。
{:important}

|字段|详细信息|
| --------- | ----------- |
| 操作系统附加组件 | 如果选择每月计费，那么可以选择以下映像附加组件：<br><br> **R1Soft Server Backup Manager** 提供高性能磁盘到磁盘服务器备份以及中央管理和数据存储库。如果选择 R1Soft 附加组件，必须购买 R1Soft 备份代理程序包，这是**服务**部分的 CDP 附加组件。仅选择其中一个会导致订单出错。有关 R1Soft 和 IBM Cloud 的更多信息，请参阅 [R1Soft Server Backup Manager ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/cloud/backup-and-restore?mhq=R1Soft%20Server%20Backup%20Manager&mhsrc=ibmsearch_a){: new_window}。<br><br>**Veeam Backup and Replication** 将自动备份与复原和复制功能相结合。Veeam 还提供高级监视、报告和容量规划。 有关 Veeam Backup and Replication 的更多信息，请参阅[带有 IBM 存储器的 Veeam Backup and Replication ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www-356.ibm.com/partnerworld/gsd/solutiondetails.do?solution=54724&lc=en&stateCd=P&tab=2){: new_window}。<br><br>**VMware vCenter** 自动部署为实现灵活、可定制的 VMware 解决方案而需要的底层 VMware vSphere 和 VMware vCenter Server 层。有关 vCenter on IBM Cloud 的更多信息，请参阅[关于 vCenter Server on IBM Cloud ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/downloads/cas/L7RKPZND?mhq=vmware%20vcenter&mhsrc=ibmsearch_a){: new_window}。|
|控制面板软件|如果选择每月计费，那么可以添加用于 Web 托管的控制面板。|
| 数据库软件      | 您可以选择要安装的数据库软件。{{site.data.keyword.cloud_notm}} 支持供应过程中部署的任何数据库软件。您也可以在部署服务器之后，安装自己的数据库软件。|
|服务|根据您所选的计费和映像，将自动为您选择一些服务。您可以从实例的任何剩余服务附加组件中进行选择。|
|供应脚本|供应脚本通常用于向服务器应用特定于客户的配置，以及帮助自动实施缩放策略。供应脚本可以是操作系统 (OS) 可运行的任何文件，包括组合二进制文件或操作系统支持的任何语言。无法在 cloud-init 映像上使用供应脚本。有关更多信息，请参阅[供应脚本](/docs/vsi?topic=virtual-servers-provisioning-scripts)。|
| 用户数据        | 您可以添加自动执行公共配置任务或运行脚本的用户数据。用户数据可以在 cloud-init 和非 cloud-init 映像上使用。|
{: caption="表 2. 公共实例附加组件" caption-side="top"}

### 连接的存储器磁盘

如果需要额外的存储空间，那么可以将存储器磁盘连接到实例。可供您使用的存储器磁盘类型取决于您选择的概要文件。例如，均衡本地概要文件和少数 GPU 概要文件使用本地支持的磁盘。 如果选择每月计费，那么可以添加 {{site.data.keyword.backup_notm}} 并选择最适合您的需求的选项。有关更多信息，请参阅 [{{site.data.keyword.backup_notm}} 服务](/docs/infrastructure/Backup?topic=Backup-getting-started)。

### 网络接口

|字段|详细信息|
| -------- | ----------- |
| 上行端口速度 | 您可以为实例选择上行链路速度，最高为 1 GB/秒。这些虚拟上行链路通过 IBM 公用网络和专用网络的冗余物理上行链路进行支持。在订购时，公用速度和专用速度始终相同，但可根据需要选择升级或降级链路。|
| 专用和公共安全组 |您可以使用安全组来制定一组 IP 过滤规则，用于定义如何处理与实例的公共接口和专用接口的传入和传出流量。有关更多信息，请参阅[关于 IBM 安全组](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups)。 |
| 专用和公共 VLAN |缺省情况下，虚拟服务器实例将放置在自动分配的 VLAN 上。如果所选的数据中心中已有一个 VLAN，那么可以选择其他 VLAN。有关更多信息，请参阅[关于 VLAN](/docs/infrastructure/vlans?topic=vlans-about-vlans)。|
| 专用和公共子网 |选择子网是可选的，仅当需要设备使用子网中的 IP 地址时才使用。如果选择子网，请验证是否有足够的 IP 地址来执行该请求。如果子网没有足够的 IP 地址，那么您的订单可能会延迟或取消。
有关更多信息，请参阅[关于子网和 IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips)。|
{: caption="表 3. 网络接口选项" caption-side="top"}

### 网络接口附加组件

|字段|详细信息|
| -------- | ----------- |
|带宽| 针对具有公共上行链路的每月实例包含 250 GB。与超额费率相比，可以购买更大的分配量，同时成本更低。|
| 硬件和软件防火墙  |防火墙服务可阻止意外流量到达服务器，减少攻击可能性，并允许服务器资源专用于目标用途。
|
| 主 IP 地址 | 主 IP 地址会自动分配给您的实例。|
| 公共辅助 IP 地址 | 在虚拟服务器实例期间您拥有这些子网。您可以单独取消子网，但如果取消实例，还会除去子网。有关更多信息，请参阅[关于子网和 IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips)。|
| IPv6 和公共静态 IPv6 地址 | 您可以为实例选择 IPv6 地址或公共静态 IPv6 地址。|
| VPN 管理 | 对于具有无限 SSL VPN 用户的实例，将自动选择此选项。有关更多信息，请参阅[关于 VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn)。|
{: caption="表 4. 网络接口附加组件" caption-side="top"}


## 通过客户门户网站供应公共实例
要通过 {{site.data.keyword.slportal}} 来供应公共虚拟服务器实例，请完成以下步骤：

  1. 使用您的唯一凭证来登录到 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。
  2. 找到**订购**部分，然后单击**设备**。
  3. 在“设备”页面上，对其中一个虚拟服务器产品，单击**每小时 SAN**、**每小时本地**、**每月**或**瞬态**。
  4. 在*配置云服务器*页面上，填写所有相关信息。
  5. 单击**添加到订单**以继续。
  6. 确认或编辑服务器的域信息。
  7. 单击**云服务条款**和**第三方服务协议**复选框。
  8. 确认或输入付款信息，然后单击**提交订单**。这会将您重定向到具有供应订单号的屏幕。您可以打印该屏幕，因为这也是您的供应订单收据。

## 后续步骤
将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件将包含一个链接，用于在您登录到 {{site.data.keyword.Bluemix_notm}} 后转至*设备详细信息*页面。

虚拟服务器已供应并可供使用后，可以使用 {{site.data.keyword.cloud_notm}} 控制台或 {{site.data.keyword.slapi_short}} 来配置虚拟服务器。有关更多信息，请参阅[配置虚拟服务器](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)。
