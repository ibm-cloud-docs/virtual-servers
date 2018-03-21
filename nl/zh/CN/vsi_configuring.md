---



copyright:
  years: 2017
lastupdated: "2017-10-25"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 配置虚拟服务器
{: #configuring-virtual-servers}

您有权访问虚拟服务器时，请确保对其进行配置以满足您环境的需求。
{:shortdesc}

## 登录 
使用初始创建帐户时通过电子邮件收到的凭证，登录到 [{{site.data.keyword.slportal_full}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。

## 找到虚拟服务器
在 {{site.data.keyword.slportal}}的“设备列表”中找到您的虚拟服务器。通过“设备列表”，可以管理设备，升级设备，或生成带宽使用量图表。有关更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。

## 记录 IP 地址和凭证
在安全位置记录服务器的 IP 地址和凭证的日志，这样无需登录到 {{site.data.keyword.slportal}}，就可快速访问这些内容。 
- 各设备 IP 地址可以在“设备列表”中查看。
- 各设备 root 用户密码可以在设备的“快照”视图中查看。单击设备名称旁边的箭头可展开该视图。
- 可以使用“设备列表”中的“下载 CSV”操作来查看多个设备 IP 地址。通过“设置”齿轮图标选择“下载 CSV”可下载电子表格格式的设备和详细信息的完整列表。

## 更新软件凭证
在供应过程中装入到设备上的所有软件都已分配有临时凭证。这些凭证在 {{site.data.keyword.slportal}}中每个设备的“密码”选项卡上进行查看和管理。第一次访问软件时，请使用这些临时凭证。作为最佳实践，请在首次访问软件后更改软件密码。请使用由字母、数字和符号组合构成的高强度密码。

（可选）可以在每个设备的“密码”选项卡上存储密码更新；但是，请务必了解，在 {{site.data.keyword.slportal}}中存储密码时，有权访问该帐户以及具有相应许可权的任何人员都可以在“密码”屏幕上查看存储的密码。

有关查看和管理软件凭证的更多信息，请参阅[管理基础架构访问权](../iam/mnginfra.html)。

## 在专用网络上访问服务器
专用网络是使用基于 IP 的 SSH 和 KVM 通过远程桌面 (RDP) 与设备进行交互的先驱者。“VPN 访问”工具支持与最近的 SSL VPN 端点或您选择的端点建立专用网络连接。此外，要与提供的多种服务进行交互，也需要 VPN 访问。有关更多信息，请参阅[虚拟专用联网 (VPN) 入门](../infrastructure/iaas-vpn/getting-started.html)。

## 设置监视服务
监视服务主要用作一种资源来检查服务器的正常运行时间，但也可用于确定何时进行扩展。标准监视服务和 Nimsoft 监视服务都可用于满足各种监视需求。标准监视服务（有时称为“基本监视服务”）通常使用通过 {{site.data.keyword.slportal}}启动的缓慢或服务 ping，用于“执行 ping 操作并获取响应”方法。Nimsoft 监视服务也称为“高级监视服务”，在以下三个层中提供：Basic、Advanced 和 Premium。此服务也可通过 {{site.data.keyword.slportal}}进行访问。有关更多信息，请参阅[监视](../infrastructure/SLmonitoring/monitoring_index.html)。

## 保证系统安全
硬件防火墙可用于确保您的设备始终安全。硬件防火墙可根据需要进行供应，无需停机。如果正确建立了规则，那么防火墙可以保护服务器免受不需要的活动打扰。订购防火墙后，必须启用该防火墙，并且必须设置规则。了解有关如何最充分地利用防火墙的更多信息。

有关更多信息，请参阅以下安全主题集合。

* [硬件防火墙（共享）](../infrastructure/hardware-firewall-shared/getting-started.html)
* [硬件防火墙（专用）](../infrastructure/hardware-firewall-dedicated/getting-started.html)

安全组是用于限制虚拟服务器上网络流量的另一个选项。可以使用安全组来制定一组 IP 过滤规则，用于定义如何处理与虚拟服务器实例的公共接口和专用接口的传入和传出流量。有关更多信息，请参阅[安全组入门](/docs/infrastructure/security-groups/sg_index.html)。

## 安排备份 
备份可确保数据安全地存储在设备外部并得到保护，避免发生数据丢失的情况。以下备份服务可用于将数据存储在安全位置，以防您需要将信息重装到设备上：
- EVault Backup 是一种基于代理程序的自动备份系统，也是一种常用的“设置后不管”设备管理解决方案，它通过额外插件包含 Exchange 和 SQL，从而兼容 Microsoft 软件。EVault 用户通过 EVault 的基于 Web 的 WebCC 应用程序与此服务进行交互。有关更多信息，请参阅[备份服务入门](../infrastructure/Backup/index.html)。
- R1Soft Continuous Data Protection 是可安装在服务器或自我管理虚拟机上的备份软件。如果您希望在单个界面上管理所有备份，那么建议使用此软件。您可通过专有管理系统与 R1Soft CDP 进行交互，这将支持在虚拟机上安装代理程序，并提供数据库插件以获得额外功能。有关更多信息，请参阅[备份服务入门](../infrastructure/Backup/index.html)。

## 后续步骤
配置虚拟服务器后，即可以开始对其进行管理。有关更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。



