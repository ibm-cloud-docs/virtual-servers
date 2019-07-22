---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 编辑可移植存储器描述
{: #editing-a-portable-storage-description}

可以在 {{site.data.keyword.cloud}} 控制台中查看可移植存储卷 (PSV)。“可移植存储器”页面会显示 PSV 的描述、位置、容量以及与 PSV 关联的设备名。您可以随时更新描述。将每个 PSV 描述更新为与使用 PSV 相关的唯一标识。
{:shortdesc}

## 开始之前
首先，导航至存储器菜单，并确保您具有完成任务的正确帐户许可权。

* 导航至控制台的存储器菜单。有关更多信息，请参阅[导航至设备](/docs/vsi?topic=virtual-servers-navigating-devices)。
* 确保您具有任何必需的帐户许可权和设备访问权。只有帐户所有者或具有**管理用户**经典基础架构许可权的用户才能调整许可权。

有关许可权的更多信息，请参阅[经典基础架构许可权](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理设备访问权](/docs/vsi?topic=virtual-servers-managing-device-access)。

## 编辑可移植存储器描述

1. 从**存储器**菜单中，选择**块存储器**。
2. 在**可移植存储器**部分中，找到要编辑的可移植存储卷。使用**过滤可移植存储器**工具以快速找到卷。
3. 单击可移植存储卷的**描述**部分以打开描述进行编辑。
4. 根据需要，在**描述**字段中输入或修改内容。
5. 单击包含 PSV 的行中的任意位置以保存已编辑的描述。

## 后续步骤

编辑 PSV 的描述后，它将保留在列表中的原始位置，直到您退出“可移植存储器”页面。重新打开此页面时，PSV 将根据描述的字母顺序出现在新位置。如果在重新启动屏幕后，PSV 不在此列表中，请在按住 **CTRL** 键的同时单击**刷新**按钮以清除浏览器的高速缓存，然后重试。可随时通过重复上述步骤来再次更改描述。
