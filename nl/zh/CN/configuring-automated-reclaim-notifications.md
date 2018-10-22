---



copyright:
  years: 2018
lastupdated: "2018-05-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 配置瞬态虚拟服务器的回收通知

瞬态虚拟服务器本质上是临时的，可以随时终止，终止时可能导致数据丢失。自动回收通知可以帮助减少丢失的数据。供应时，瞬态虚拟服务器可以配置为在实际终止前 **2 分钟**接收到关于即将终止的通知。通知支持以编程方式提醒瞬态虚拟服务器完成正在执行的任何处理，或者转移瞬态虚拟服务器上的任何必要数据。

`reclaim-scheduled` 通知是 Webhook，这意味着 HTTP POST 请求会将通知发送给用户提供的端点。完成以下步骤以设置并使用 Webhook：

1. 供应瞬态虚拟服务器实例。
2. 设置 Webhook。
3. 验证 Webhook 请求。

## 供应瞬态虚拟服务器实例

瞬态虚拟服务器可以通过 [{{site.data.keyword.slportal_full}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window} 或通过 [SLDN API ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://sldn.softlayer.com){: new_window} 供应。有关更多信息，请参阅[供应瞬态实例](/docs/vsi/vsi_provision_transient.html)。


## 设置 Webhook

要设置 Webhook，您需要使用 SLDN API 将以下参数指定到瞬态虚拟服务器实例：

   * **URI** - 向其发送 `reclaim-scheduled` 通知的有效 HTTP URI。
   * **密码** - 一个字符串，用作签署请求的散列算法的密钥。不要将密码字符串告诉其他任何人。

必须为供应的每个瞬态虚拟服务器设置 Webhook。但是，URI 和密钥不需要唯一。

两个参数都是必需的。如果必须更改 URI 或密码，请使用新信息再次调用该方法。
{: tip}

可以使用以下方法通过 SLDN API 设置瞬态虚拟服务器 Webhook。

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

有关更多信息，请参阅 SLDN API 方法文档进行 [Webhook 设置 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}。

### 取消 reclaim-scheduled 通知

要取消 `reclaim-scheduled` 通知，请调用以下 SLDN API 方法：

  `SoftLayer_Virtual_Guest::deleteWebhook()`

有关更多信息，请参阅 SLDN API 方法文档的[取消通知 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}。

## 验证 Webhook 请求

要验证 `reclaim-scheduled` 通知，请检查以下项：

1. 请求的时间戳记

   根据请求头中的时间戳记检查接收请求的时间。如果请求已发出超过大约 30 秒，请不要接受请求。此操作有助于防止重放攻击。

2. 请求的“X-IBM-Nonce”头中发现的现时标志

   此值是发送请求时随机生成的字符串。您可以选择存储先前接收的现时标志，以与请求中包含的现时标志进行比较。如果先前使用了请求中的现时标志，那么不要接受请求。此操作有助于防止重放攻击。

3. 位于请求的“Authorization”头中的散列消息认证代码 (HMAC)

   此值是使用 HMAC-SHA256 算法（该算法使用所提供的密码字符串作为密钥）进行散列化，然后编码为 Base64 的字符串。您需要构造字符串，进行散列化并将其编码为 Base64，然后将结果与“Authorization”头中的签名进行比较。如果不匹配，不要接受请求。请参阅下一部分以获取有关创建 HMAC 签名的详细信息。

### 比较 HMAC 签名

为了验证请求的“Authorization”头中的 HMAC 签名，您需要创建比较字符串。完成以下步骤以创建字符串：

1. 创建规范字符串。

  规范字符串必须包含以下数据：
  * 方法类型 - 在本例中为 POST（必须大写）
  * 内容类型 - 位于“Content-Type”头中
  * 有效内容 - 请求的主体。此示例假定 JSON 字符串已解码成本机关联数组或字典。  
  * 现时标志 - 位于“X-IBM-Nonce”头中

  要创建规范字符串，请在不使用分隔符的情况下，将规范字符串数据严格按以下顺序组合起来：

  方法类型 + 内容类型 + 有效内容['id'] + 有效内容['serviceName'] + 有效内容['event'] + 有效内容['time stamp'] + 现时标志

2. 散列化规范字符串。

  瞬态虚拟服务器 Webhook 中使用的散列算法为 HMAC-SHA256，这是一种密钥散列算法。要使用的密钥是设置 Webhook 时提供的密码。

3. 将散列化的规范字符串编码为 Base64。

4. 将生成的字符串与“Authorization”头中的签名进行比较。  

  使用可防止计时攻击的字符串比较函数。如果字符串不匹配，不要接受请求。

## `reclaim-scheduled` 通知请求有效内容的剖析

从瞬态虚拟服务器 Webhook 发送的请求与任何 HTTP 请求的相似之处在于，它有头和有效内容。有效内容是以下形式的 JSON 格式字符串：

**注**：不能保证键名采用此特定顺序。

	{
		'event': 'reclaim-scheduled',
		'id': <string - that is the ID of the transient guest being reclaimed>,
		'link': <string - link for an API call to return info about the guest being reaped>,
		'serviceName': <string - name of the API service class>,
		'time stamp': <integer - timestamp of when the reclaim was scheduled>
	}


## 创建 HMAC 签名的代码示例

Python：

```
# This assumes that the request headers are stored in a dictionary called headers and that the JSON
# content of the request has been decoded into a dictionary called payload.

import base64
import hashlib
import hmac

secret = 'Your secret key'
canonical = 'POST' + headers['Content-Type'] + payload['id'] + payload['serviceName'] + payload['event'] \
	    + payload['timestamp'] + headers['X-IBM-Nonce']
signature = base64.b64encode(hmac.new(secret, canonical, hashlib.sha256).hexdigest())
match_flag = hmac.compare_digest(headers['Authorization'], signature)
```
{: screen}

PHP：

```
// This assumes that the request headers are stored in an associative array called $headers and that
// the JSON content of the request is decoded into an associative array called $payload.

$secret = 'Your secret key';
$canonical = 'POST' . $headers['Content-Type'] . $payload['id'] . $payload['serviceName'] . $payload['event']
	     . payload['time stamp'] . $headers['X-IBM-Nonce'];
$signature = base64_encode(hash_hmac('sha256', $canonical, $secret));
$matchFlag = hash_equals($headers['Authorization'], $signature); 
```
{: screen}

Node.js：

```
// This assumes that the request headers are stored in variables that are named content_type, nonce, and auth_string.
// This also assumes that the content of the request is a JSON object called payload.

const crypto = require('crypto');

var canonical = 'POST' + content_type + payload.id + payload.serviceName + payload.event + payload.timestamp + nonce;
hmac = crypto.createHmac('sha256', secret).update(canonical);
signature = Buffer.from(hmac.digest('hex')).toString('base64');
matchFlag = crypto.timingSafeEqual(auth_string, signature);
```
{: screen}
