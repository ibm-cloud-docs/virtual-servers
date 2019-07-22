---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# 虚拟服务器实例的资源注意事项
{: #capacity-considerations}

## 问题描述

供应虚拟服务器时，可能会收到以下错误消息：

```
没有足够的容量来完成请求。
```
{:screen}

供应失败时，该特定请求中的所有虚拟服务器实例均会失败。
{:tip}

## 问题原因

路由器或数据中心的可用资源不足而无法满足服务请求时，会发生错误。有多个原因可能会导致您收到此错误。资源可用性变化频繁，因此您可以等待并稍后重试。

## 解决方法

可以尝试使用以下策略重新进行供应：

1. 指定其他路由器进行供应。  
2. 在不指定路由器的情况下进行供应。
3. 在其他数据中心内进行供应。
4. 供应更少的实例。
5. 通过供应到多个数据中心来分布实例。
6. 供应更小的实例大小。
7. 将 VSI 存储器从 SAN 变更为 LOCAL，或从 LOCAL 变更为 SAN。
