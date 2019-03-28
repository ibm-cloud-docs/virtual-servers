---

copyright:
  years: 2018
lastupdated: "2018-08-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 分配服务器 IP 地址
{: #assigning-server-ip-addresses}

{{site.data.keyword.cloud}} 将虚拟服务器实例配置为使用专用网络上的 IPv4 地址，并可根据请求，配置为使用公共（面向因特网）IPv4 地址。此外，您可以请求公用网络上的 IPv6 地址。所有这些 IP 地址统称为_主 IP 地址_。
{:shortdesc}

通过 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com) 购买辅助子网后，可以将更多 IP 地址绑定到虚拟服务器实例。以这种方式购买并由您管理的 IP 地址称为_辅助 IP 地址_。

有关可用于获取 IP 地址的选项的更多信息，请参阅[子网和 IP](/docs/infrastructure/subnets?topic=subnets-getting-started-with-subnets-and-ips#getting-started-with-subnets-and-ips)。

## 绑定辅助 IP 地址

购买并路由辅助子网后，必须将操作系统配置为使用一个或多个新近可用的 IP 地址。对于每种操作系统，新 IP 地址的配置步骤各不相同，但设置通常称为设置“接口别名”。有关其他配置详细信息，请参阅操作系统文档。
