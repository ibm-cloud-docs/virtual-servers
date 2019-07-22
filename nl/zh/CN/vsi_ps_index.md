---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# 供应脚本
{: #provisioning-scripts}

供应脚本是供应过程中可以下载到设备或者下载并在设备上运行的脚本。对于现有帐户，供应脚本在 {{site.data.keyword.cloud_notm}} 控制台中管理。在订购过程中，您可以手动输入新帐户的脚本或者尚未跟踪的脚本。

或者，也可以使用支持 cloud-init 的映像并提供用户数据来自动执行配置任务或运行脚本。有关更多信息，请参阅[使用支持 cloud-init 的映像进行供应](/docs/infrastructure/image-templates?topic=image-templates-provisioning-with-a-cloud-init-enabled-image)。
{: tip}

在供应过程中，与 HTTP URL 关联的脚本将下载到设备。供应之后，管理员必须在设备上手动运行脚本。将自动下载并运行与 HTTPS URL 关联的脚本。供应脚本当前在标准的 Linux 操作系统（Cent、RHEL、Fedora、Debian 或 Ubuntu）以及 Windows 和 FreeBSD 上可用。不支持其他系统，例如 Vyatta、Netscaler、XenServer、VMware。供应脚本可以是操作系统运行的任何类型的文件，包括组合二进制文件或操作系统支持的任何语言。

有关更多信息，请参阅[管理供应脚本](/docs/vsi?topic=virtual-servers-managing-a-provisioning-script#managing-a-provisioning-script)。
