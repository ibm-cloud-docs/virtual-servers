---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 启动急救内核 
{: #launching-rescue}

急救内核是一种实时急救环境，旨在让客户有能力使裸机服务器或虚拟服务器联机，从而对通常只能通过操作系统重装来解决的系统问题进行故障诊断。急救内核必须在 {{site.data.keyword.slportal_full}}上启动。要为设备启动急救内核，请使用以下步骤。
{:shortdesc}

## 启动急救内核

1. 使用您的唯一凭证来访问 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/)。
2. 在“设备列表”中，单击要急救的设备的名称。
3. 单击右上角的*操作*下拉列表，然后选择**急救**。
4. 单击**是**按钮以将设备立即转换为急救内核。单击**否**按钮以取消操作。

## 后续步骤
启动急救内核后，设备会断电并重新引导到设备操作系统的急救内核。这可能需要几分钟时间。

通过设备的 IP 地址，可对该设备进行远程访问。在急救内核中，可以使用在 {{site.data.keyword.slportal}}上记录的设备 root 用户或管理员凭证来访问设备。使用急救内核时，可以像在定期引导的设备上一样执行故障诊断、发现问题和解决问题。如果需要，可以将驱动器安装到急救内核操作系统中。要退出急救内核并使设备恢复为其常规环境，请在 {{site.data.keyword.slportal}}中重新引导设备，或通过急救内核操作系统进行重新引导。

有关重新引导设备的更多信息，请参阅[管理虚拟服务器](../vsi/vsi_managing.html)。

