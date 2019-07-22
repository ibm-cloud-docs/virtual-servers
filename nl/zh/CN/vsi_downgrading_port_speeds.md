---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 对端口速度降级
{: #downgrading-port-speeds}

您可以临时对虚拟服务器实例的端口速度降级，而无需开具凭单。您最多只能对已付费的任何端口执行降级、断开连接或重新连接操作。不能通过此选项进行升级。更改会保留在控制台中，直到您将其还原。此操作不会更改帐单，所以临时对服务器降级不会使帐单金额变少。如果需要对端口速度进行永久性更改，您必须开具销售凭单。
{:shortdesc}

## 开始之前
首先，导航至设备菜单，并确保您具有完成任务的正确帐户许可权。 

* 导航至控制台的设备菜单。有关更多信息，请参阅[导航至设备](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 确保您具有任何必需的帐户许可权和设备访问权。只有帐户所有者或具有**管理用户**经典基础架构许可权的用户才能调整许可权。 

有关许可权的更多信息，请参阅[经典基础架构许可权](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理设备访问权](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 对端口速度降级
要对端口速度降级，请完成以下步骤。

1. 在**设备**菜单中，选择**设备列表**。
2. 选择要更新的服务器。
3. 在**概述**选项卡中，转至**网络详细信息**。
4. 选择**速度**中的下拉菜单（对于公用或专用网络）以对端口速度降级或断开与端口的连接。

出于任何原因更改端口速度或断开端口连接时，必须手动更改服务器本身。
{:tip}
