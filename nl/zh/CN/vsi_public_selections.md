---

copyright:
  years: 2017, 2018
lastupdated: "2018-02-12"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 供应选择内容
{: #provisioning-selections}

在供应公共虚拟服务器时，必须进行以下选择。

## 位置
可以选择要部署到的特定数据中心。对于新部署，{{site.data.keyword.Bluemix}} 会自动识别最佳数据中心（基于可用性）并创建相应的公用和专用 VLAN。要向现有环境添加项，可以选择您的设计所需的特定数据中心、VLAN 和子网。有关 VLAN 和子网的更多信息，请参阅 [VLAN 入门](/docs/infrastructure/vlans?topic=vlans-getting-started-with-vlans)。

选择子网是可选的，仅当需要设备使用子网中的 IP 地址时才使用。如果选择子网，请验证是否有足够的 IP 地址来执行该请求。如果子网没有足够的 IP 地址，那么您的订单可能会延迟或取消。
{:tip}

## 处理器/RAM
订购时，有多个核心处理器选项可供选择。核心处理器选项遵循虚拟服务器部署的标准。服务器上的每个物理核心都是超线程核心，并显示为两个虚拟 CPU (vCPU) 或核心。虚拟服务器产品提供了每个核心 2.0 GHz 或更高的性能，最多可在单个虚拟服务器上提供 56 个核心。

RAM 是极为简单的存储器。该产品将您选择的 RAM 量全部专用于您的虚拟服务器，在单个虚拟服务器上最高可达 242 GB。

**注**：公共实例和专用实例的最大配置值略有不同。如果分配的核心数或内存极高，将限制可用的选项。

## 操作系统

还需要选择要部署到服务器的操作系统。您有若干免费选项可选择，例如 CentOS 和 Ubuntu。另外，还提供了付费选项，例如 Windows Server 和 Red Hat EnterpriseLinux (RHEL)。值得注意的是 Windows 需要一个 100 GB 的主磁盘。

对于现有客户，还可以通过{{site.data.keyword.slportal_full}}浏览至**设备 -> 管理 -> 映像**，并从*操作*菜单中选择**订购虚拟服务器**，以基于映像模板进行部署。这将自动为订单选择相应的操作系统。或者，可以基于标准映像进行订购，然后随时重装到映像模板。

## 存储器

可以为每个虚拟服务器选择 SAN 或本地存储器。您可以根据需要使用其他存储产品作为 SAN 或本地存储器的补充。SAN 和本地存储器均作为本地磁盘公开给虚拟服务器。对磁盘进行的任何更改（例如，连接、拆离和迁移等）都需要重新引导虚拟服务器。有关更多信息，请参阅[存储器选项](/docs/vsi?topic=virtual-servers-storage-options#storage-options)。

## 按小时和按月计费

可以为虚拟服务器选择按小时或按月计费。除了成本外，主要的差异在于每小时服务器没有包含带宽分配量。在结算周期结束时，将计算帐户上每个服务器的带宽使用量和处于活动状态的小时数。在 {{site.data.keyword.slportal}}的“虚拟服务器视图”页面下，提供了汇总，并有“详细信息”页面的链接，其中显示每个行项、小时数和每项的运行费用。

## 带宽

产品针对具有公共上行链路的每月虚拟服务器包含 250 GB。与超额费率相比，可以购买更大的分配量，同时成本更低。

## 端口速度

可以为虚拟服务器选择上行链路速度，最高 1 GB/秒。这些虚拟上行链路通过 IBM 公用网络和专用网络的冗余物理上行链路进行支持。在订购时，公用速度和专用速度始终相同，但可根据需要选择升级或降级链路。

## 软件

可以选择在供应过程中由 {{site.data.keyword.Bluemix_notm}} 安装软件。{{site.data.keyword.Bluemix_notm}} 支持在供应过程中部署的任何软件。您也可以在部署服务器之后，安装自己的软件。

## 安全性

部署之前，请考虑安全性选项。在订购过程中，可以选择特定于设备的硬件或软件防火墙来提供保护。或者，可以将专用防火墙设备部署到环境，然后将虚拟服务器部署到受保护的 VLAN。

**注**：一个虚拟服务器不能由同一接口上的两个防火墙设备进行保护。

还可以使用安全组来制定一组 IP 过滤规则，用于定义如何处理与虚拟服务器实例的公共接口和专用接口的传入和传出流量。

有关更多信息，请参阅以下安全主题集合。

* [Hardware Firewall (Shared)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-getting-started-with-hardware-firewall-shared)
* [Hardware Firewall (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-getting-started-with-hardware-firewall-dedicated)
* [安全组入门](/docs/infrastructure/security-groups?topic=security-groups-getting-started-with-security-groups)

## 监视服务
{: #about-monitoring}

可以从虚拟服务器的各种监视服务选项中进行选择。选项包括标准监视服务，该服务通过 Ping 和传输控制协议 (TCP) 服务响应进行监视，并且在发生故障时包含可选的响应。您还可以添加高级监视服务，该服务使用 Nimsoft 软件代理程序提供了一组更丰富的功能来监视虚拟服务器和已安装的软件。

有关更多信息，请参阅[监视](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring)。

## 备份

在订购过程中，可以添加 {{site.data.keyword.backup_notm}}。还可以选择购买现有 R1soft 备份环境的 R1soft 许可证，或利用第三方备份解决方案。

有关更多信息，请参阅[重新注册保险库](/docs/infrastructure/Backup?topic=Backup-reregister#reregister)。

## 供应后脚本

供应后脚本可以与任何虚拟服务器订单相关联。这将在完成其他供应任务后运行客户开发的脚本。这些脚本通常用于向服务器应用特定于客户的配置，以及帮助自动实施缩放策略。

有关更多信息，请参阅[添加定制供应脚本](/docs/vsi?topic=virtual-servers-adding-post-script)。

## 接下来做什么？
准备好供应公共虚拟服务器后，请参阅[供应公共实例](/docs/vsi?topic=virtual-servers-ordering-vs-public)。
