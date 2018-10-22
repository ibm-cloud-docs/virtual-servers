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

# 配置暫時性虛擬伺服器收回通知

暫時性虛擬伺服器本質上是暫時存在的，隨時都可以終止，因此可能會導致遺失資料。自動化收回通知有助於減少資料遺失。佈建時，暫時性虛擬伺服器可以配置成在實際終止之前的**兩分鐘**收到將終止的通知。通知可讓您以程式設計方式警告暫時性虛擬伺服器完成任何進行中的處理，或將任何必要資料傳送離開暫時性虛擬伺服器。

`reclaim-scheduled` 通知是一種 Webhook，這表示通知會由 HTTP POST 要求傳送給使用者提供的端點。請完成下列步驟，以設定及使用 Webhook：

1. 佈建暫時性虛擬伺服器實例。
2. 設定 Webhook。
3. 驗證 Webhook 要求。

## 佈建暫時性虛擬伺服器實例

可以透過 [{{site.data.keyword.slportal_full}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window} 或透過 [SLDN API ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://sldn.softlayer.com){: new_window} 佈建暫時性虛擬伺服器。如需相關資訊，請參閱[佈建暫時性實例](/docs/vsi/vsi_provision_transient.html)。

## 設定 Webhook

若要設定 Webhook，您需要使用 SLDN API，將下列參數指派給暫時性虛擬伺服器實例：

   * **URI** - `reclaim-scheduled` 通知的傳送目標有效 HTTP URI。
   * **密碼** - 用來作為雜湊演算法簽署要求之金鑰的字串。請不要告知任何其他人密碼字串。

必須為每一部已佈建的暫時性虛擬伺服器設定 Webhook。不過，URI 及密碼不需要是唯一的。

這兩個參數都是必要參數。如果必須變更 URI 或密碼，則請使用新的資訊來重新呼叫方法。
{: tip}

可以使用下列方法，透過 SLDN API 來設定暫時性虛擬伺服器 Webhook：

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

如需相關資訊，請參閱 SLDN API 方法文件以了解 [Webhook 設定 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}。

### 取消 reclaim-scheduled 通知

若要取消 `reclaim-scheduled` 通知，請呼叫下列 SLDN API 方法：

  `SoftLayer_Virtual_Guest::deleteWebhook()`

如需相關資訊，請參閱[取消通知 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window} 的 SLDN API 方法文件。

## 驗證 Webhook 要求

若要驗證 `reclaim-scheduled` 通知，請檢閱下列項目：

1. 要求的時間戳記

   根據要求標頭中的時間戳記，檢查收到要求的時間。如果關閉超過大約 30 秒，請勿接受要求。此動作有助於防止重播攻擊。

2. 在要求的 "X-IBM-Nonce" 標頭中發現的 Nonce

   這個值是在傳送要求時隨機產生的字串。您可以選擇儲存先前收到的 Nonce，以與要求中所含的 Nonce 進行比較。如果先前使用過要求中的 Nonce，請不要接受要求。此動作有助於防止重播攻擊。

3. 「雜湊訊息鑑別碼 (HMAC)」位於要求的 "Authorization" 標頭中

   這個值是一個使用 HMAC-SHA256 演算法進行雜湊處理，然後編碼為 Base64 的字串，而 HMAC-SHA256 演算法則使用所提供的密碼字串作為金鑰。您需要建構字串、對字串進行雜湊處理、將字串編碼為 Base64，然後比較結果與 "Authorization" 標頭中的簽章。如果不相符，請勿接受要求。如需建立 HMAC 簽章的詳細資料，請參閱下節。

### 比較 HMAC 簽章

若要驗證位於要求之 "Authorization" 標頭中的 HMAC 簽章，您需要建立比較字串。完成下列步驟，以建立字串：

1. 建立標準字串。

  標準字串必須包含下列資料：
  * 方法類型 - 在此情況下為 POST（必須為大寫）
  * 內容類型 - 位於 "Content-Type" 標頭中
  * 有效負載 - 要求的內文。此範例假設 JSON 字串解碼為原生關聯式陣列或字典。  
  * Nonce - 位於 "X-IBM-Nonce" 標頭中

  若要建立標準字串，請以下列確切順序且不含定界字元，來結合標準字串資料：

  方法類型 + 內容類型 + 有效負載['id'] + 有效負載['serviceName'] + 有效負載['event'] + 有效負載['time stamp'] + Nonce

2. 將標準字串進行雜湊處理。

  暫時性虛擬伺服器 Webhook 中所使用的雜湊演算法為 HMAC-SHA256，其為含金鑰的雜湊演算法。要使用的金鑰就是設定 Webhook 時所提供的密碼。

3. 將雜湊的標準字串編碼為 Base64。

4. 比較產生的字串與 'Authorization' 標頭中的簽章。  

  使用時序攻擊安全字串比較函數。如果字串不相符，請勿接受要求。

## `reclaim-scheduled` 通知要求有效負載的結構

從暫時性虛擬伺服器 Webhook 傳送的要求就像任何 HTTP 要求一樣，會有標頭及有效負載。有效負載是下列形式的 JSON 格式化字串：

**附註**：不保證金鑰名稱是按照此特定順序。

	{
		'event'：'reclaim-scheduled',
		'id'：<字串 - 這是所收回之暫時性訪客的 ID>、
		'link'：<字串 - 傳回所回收訪客相關資訊之 API 呼叫的鏈結>、
		'serviceName'：<字串 - API 服務類別的名稱>、
		'time stamp'：<整數的 - 排程收回的時間戳記>
	}


## 建立 HMAC 簽章的程式碼範例

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
