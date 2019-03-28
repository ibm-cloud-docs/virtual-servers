---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 备份服务
{: #back-up-services}

## IBM Cloud Backup

{{site.data.keyword.backup_full}} 是一种基于代理程序的自动备份系统，通过 {{site.data.keyword.backup_notm}} WebCC 基于浏览器的管理实用程序进行管理，为用户提供了在 {{site.data.keyword.BluSoftlayer}} 网络上的一个或多个数据中心内的服务器之间备份数据的方法。管理员可以将备份设置为每小时、每天、每周或按定制日程安排执行，备份的目标是完整系统、特定目录，甚至是个别文件。通过其他插件，可与 Microsoft Exchange 和 Microsoft SQL 等软件以及其他类型的第三方软件兼容，并支持用户根据需要执行裸机复原。

有关 {{site.data.keyword.backup_notm}} 服务的更多信息，请参阅 [{{site.data.keyword.backup_notm}} 服务入门](/docs/infrastructure/Backup?topic=Backup-gettingstarted#gettingstarted)。

## R1Soft CDP

Continuous Data Protection (CDP) 是 R1Soft 创建的高性能备份软件，用于备份物理和虚拟设备。Idera CDP 包含三个主要组件：CDP 服务器、代理程序和数据库插件；数据库插件可与前两个组件分开购买。由于 R1Soft CDP 是第三方备份解决方案，因此与 CDP 的交互完全在 {{site.data.keyword.Bluemix_short}} 专有接口外部执行；但是，可以在 {{site.data.keyword.slportal}}中跟踪和存储 R1Soft CDP 密码。与 R1Soft CDP 的其他所有交互都会在 R1Soft Web 站点上进行记录。

有关 R1Soft CDP 备份服务的更多信息，请参阅 [R1Soft 文档 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://wiki.r1soft.com/display/ServerBackupManager/Home){: new_window}。

