---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 启动急救内核
{: #launching-rescue}

急救内核是一种实时急救环境，旨在让您可以使裸机服务器或虚拟服务器联机，从而对通常只能通过操作系统重装来解决的系统问题进行故障诊断。急救内核必须在 {{site.data.keyword.cloud}} 控制台中启动。要为设备启动急救内核，请使用以下步骤。
{:shortdesc}

## 开始之前
首先，导航至设备菜单，并确保您具有完成任务的正确帐户许可权。

* 导航至控制台的设备菜单。有关更多信息，请参阅[导航至设备](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 确保您具有任何必需的帐户许可权和设备访问权。只有帐户所有者或具有**管理用户**经典基础架构许可权的用户才能调整许可权。

有关许可权的更多信息，请参阅[经典基础架构许可权](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理设备访问权](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 启动急救内核

1. 在**设备**菜单中，选择**设备列表**。
2. 在**设备列表**中，单击要急救的设备的名称。
3. 在*操作*菜单中，选择**急救方式**。
4. 单击**是**以将设备立即转换为急救内核。

## 为 Windows 实例启动急救内核

1. 在**设备**菜单中，选择**设备列表**。
2. 在**设备列表**中，单击要急救的设备的名称。
3. 在*操作*菜单中，选择**从映像引导**。
4. 选择公共映像 *WindowsRescueStandalone.iso* 旁的**从此映像引导**。

## 后续步骤
启动急救内核后，设备会断电并重新引导到设备操作系统的急救内核。这可能需要几分钟时间。

通过设备的 IP 地址，可对该设备进行远程访问。在急救内核中，可以使用在 {{site.data.keyword.cloud_notm}} 控制台上记录的设备 root 用户或管理员凭证来访问设备。使用急救内核时，可以像在定期引导的设备上一样执行故障诊断、发现问题和解决问题。如果需要，可以将驱动器安装到急救内核操作系统中。要退出急救内核并使设备恢复为其常规环境，请在 {{site.data.keyword.cloud_notm}} 控制台中重新引导设备，或通过急救内核操作系统进行重新引导。

有关重新引导设备的更多信息，请参阅[管理虚拟服务器](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)。
