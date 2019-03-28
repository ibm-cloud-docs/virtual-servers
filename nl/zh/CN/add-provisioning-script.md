---

copyright:
  years: 2014, 2018
lastupdated: "2018-04-27"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 管理供应脚本
{: #managing-a-provisioning-script}

使用供应脚本指定要在新供应的设备上运行的脚本的 URL。脚本名称没有限制；但是，对每个脚本使用类似的命名约定可更容易进行识别。供应脚本必须与标准域名关联，并且必须可使用 HTTP 或 HTTPS 协议进行访问。当供应脚本下载到设备时，使用的协议类型会影响系统的自动响应。

* 使用 **HTTP 协议**时需要管理员在下载脚本之后手动运行脚本。
* 使用 **HTTPS 协议**时将自动下载和运行脚本（如果可能）。如果 URL 未关联到可执行脚本，那么将下载脚本，但不得执行任何进一步的操作。

## 访问供应脚本屏幕
1. 使用唯一凭证进入 [{{site.data.keyword.slportal_full}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。

2. 从导航中选择**设备 > 管理 > 供应脚本**以访问供应脚本屏幕。


## 添加供应脚本
{: #add-provisioning-script}

1. 从 {{site.data.keyword.slportal}} 的**供应脚本**屏幕，单击屏幕顶部的**添加供应脚本**。
* 在**名称**字段中，输入供应脚本的**识别名称**。
* 在 **URL** 字段中，输入与脚本相关联的**标准域名**。
* 单击**添加**以将供应脚本添加到帐户。单击**取消**可取消该操作。

## 编辑供应脚本详细信息

1. 从 {{site.data.keyword.slportal}} 的**供应脚本**屏幕，单击供应脚本的**名称**或 **URL** 列中任何位置，以打开脚本进行编辑。
3. 更新名称或 URL。
  * **注：**更新 URL 时，您必须使用标准域名，否则不会保存更改。
4. 单击屏幕上任何位置以保存编辑。

## 后续步骤

可以随时修改或除去与帐户关联的供应脚本。供应脚本在除去之前将保存在 {{site.data.keyword.slportal}} 中，并且可以与通过 {{site.data.keyword.slportal}} 订购的任何新设备相关联。如果脚本与 HTTP URL 相关联，供应期间会将该脚本下载到新设备。将下载与 HTTPS URL 关联的脚本，并且在适当的情况下，这些脚本将在新设备上运行。

编辑脚本之后，会立即在屏幕上显示有效更新。对现有供应脚本进行的更改不会影响已经供应的设备。
