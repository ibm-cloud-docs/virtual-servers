---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 管理可移植存储器
{: #accessing-portable-storage}

可移植存储卷 (PSV) 是专用于 {{site.data.keyword.virtualmachinesshort}} 的辅助存储器解决方案。在 {{site.data.keyword.cloud}} 控制台中，您可以访问可移植存储卷并显示所有 PSV。您还可以连接、拆离、交换和编辑卷。
{:shortdesc}

无法将可移植存df储卷连接或交换到通过加密映像模板供应的虚拟服务器实例。
{:note}

## 开始之前
首先，导航至存储器或设备菜单，并确保您具有完成任务的正确帐户许可权。

* 导航至控制台的存储器或设备菜单。有关更多信息，请参阅[导航至设备](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 确保您具有任何必需的帐户许可权和设备访问权。只有帐户所有者或具有**管理用户**经典基础架构许可权的用户才能调整许可权。

有关许可权的更多信息，请参阅[经典基础架构许可权](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理设备访问权](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 连接可移植存储器

1. 从**存储器**菜单中，选择**块存储器**。
2. 在**可移植存储器**部分中，选择要使用的可移植存储器的连接选项。
3. 在下一个屏幕上，选择需要存储器的设备，然后选择**连接**。

## 管理连接到服务器的可移植存储器

连接到服务器的可移植存储器列在该服务器的*设备详细信息*页面上。

1. 从**设备**菜单中，选择**设备列表**。
2. 从**设备列表**中，选择虚拟服务器实例以查看其详细信息。
3. 单击**存储器**选项卡以查看当前连接到实例的可移植存储器。
4. 在**操作**菜单中，可以**交换**或**拆离**存储器。
