---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 添加定制供应脚本 
{: #adding-post-script}

定制供应脚本支持用户指定在新供应的设备上运行的脚本的 URL。您可以在 {{site.data.keyword.slportal_full}}中发布和管理定制供应脚本。
{:shortdesc}

订购设备时，如果已将定制供应脚本发布到 {{site.data.keyword.slportal}}的“供应脚本”屏幕，那么可以选择该脚本。如果尚未添加脚本，那么可以提供相应的 URL。供应脚本可以是操作系统 (OS) 可执行的任何文件，包括组合二进制文件或任何操作系统支持的语言。要在 {{site.data.keyword.slportal}}上添加定制供应脚本，请使用以下步骤。

**注**：此功能当前仅可用于基于 Linux 和 Unix 的操作系统。

## 添加供应脚本

1. 在 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window} 的**设备**菜单中，选择**管理** > **供应脚本**。
2. 单击**添加供应脚本**。
4. 在“名称”字段中，输入唯一的脚本名称。
5. 在 URL 字段中，输入要与脚本关联的准确 URL。
6. 单击**添加**。

## 后续步骤
提交包含供应脚本的订单后，将供应与其他任何设备类似的设备。在设备变为可用之前，指定的脚本会下载到设备。供应脚本的源将确定执行供应过程中这最后一步期间的行为。如果脚本是通过 HTTPS URL 提供的，那么会下载并运行脚本，而无需用户进行其他交互。如果脚本是通过 HTTP 提供的，那么仅下载脚本。对于通过 HTTP 提供的脚本，管理员必须登录到设备，并手动运行脚本。
