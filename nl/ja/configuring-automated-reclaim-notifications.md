---

copyright:
  years: 2018
lastupdated: "2018-05-11"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# 一時仮想サーバーの再利用についての通知の構成
{: #configuring-notifications-for-reclaims-of-transient-virtual-servers}

一時仮想サーバーは、その性質として一時的であり、いつでも終了させることができますが、それが原因でデータが失われることがあります。 自動再利用通知は、消失データの削減に役立ちます。 プロビジョン時に、終了が近いという通知を実際の終了の **2 分前**に受け取るように、一時仮想サーバーを構成できます。 この通知により、ユーザーは、実行中のすべての処理を終了するように、または、必要なデータを一時仮想サーバーから転送するように、一時仮想サーバーにプログラマチックに警告することができます。

`reclaim-scheduled` 通知は Web フックです。これは、この通知が HTTP POST 要求によって、ユーザー指定のエンドポイントに送信されることを意味します。 この Web フックをセットアップおよび使用するには、以下の手順を実行します。

1. 一時仮想サーバー・インスタンスをプロビジョンします。
2. Web フックをセットアップします。
3. Web フック要求を確認します。

## 一時仮想サーバー・インスタンスのプロビジョニング
{: #provision-transient-virtual-server}

一時仮想サーバーは、[{{site.data.keyword.slportal_full}} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://control.softlayer.com/){: new_window} または [SLDN API ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://sldn.softlayer.com){: new_window} を介してプロビジョンできます。 詳しくは、[一時インスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-ordering-vs-transient)を参照してください。

## Web フックのセットアップ

Web フックをセットアップするには、SLDN API を使用して以下のパラメーターを一時仮想サーバー・インスタンスに割り当てる必要があります。

   * **URI** - `reclaim-scheduled` 通知の送信先にする有効な HTTP URI。
   * **secret** - 要求に署名するためのハッシュ・アルゴリズムの鍵として使用されるストリング。 secret ストリングは、他の人に知られないようにしてください。

プロビジョンされる一時仮想サーバーごとに Web フックのセットアップが必要です。 ただし、URI と secret は固有である必要はありません。

両方のパラメーターが必須です。 URI または secret の変更が必要な場合は、新しい情報でメソッドを再度呼び出してください。
{: tip}

以下のメソッドを使用して、SLDN API を介して一時仮想サーバー Web フックをセットアップできます。

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

詳しくは、[Web フックのセットアップ ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window} についての SLDN API メソッド資料を参照してください。

### reclaim-scheduled 通知のキャンセル

`reclaim-scheduled` 通知をキャンセルするには、次の SLDN API メソッドを呼び出します。

  `SoftLayer_Virtual_Guest::deleteWebhook()`

詳しくは、[通知のキャンセル ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window} についての SLDN API メソッド資料を参照してください。

## Web フック要求の検証

`reclaim-scheduled` 通知を検証するには、以下の項目を検討します。

1. 要求のタイム・スタンプ

   要求を受信した時刻を、要求ヘッダー中のタイム・スタンプに照らしてチェックします。 差がおよそ 30 秒を超える場合、要求を受け入れないでください。 このアクションは、リプレイ・アタックを防止するのに役立つことがあります。

2. 要求の "「X-IBM-Nonce」" ヘッダー内で見つかった nonce

   この値は、要求が送信されるときにランダムに生成されるストリングです。 前に受信した nonce を保管して、要求に組み込まれた nonce と比較することを選択できます。 要求内の nonce が前に使用されたものである場合、要求を受け入れないでください。 このアクションは、リプレイ・アタックを防止するのに役立つことがあります。

3. 要求の "Authorization" ヘッダーにある HMAC (Hash Message Authentication Code)

   この値は、指定された secret ストリングを鍵として使用する HMAC-SHA256 アルゴリズムを使用してハッシュされてから、Base64 にエンコードされたストリングです。 ストリングを作成し、ハッシュし、Base64 にエンコードし、次に、その結果を "Authorization" ヘッダー内の署名と比較する必要があります。 それらが一致しない場合、要求を受け入れないでください。 HMAC 署名の作成について詳しくは、次のセクションを参照してください。

### HMAC 署名の比較

要求の「Authorization」ヘッダーにある HMAC 署名を検証するには、比較ストリングを作成する必要があります。 そのストリングを作成するには、以下の手順を実行します。

1. 正規化されたストリングを作成します。

  正規ストリングには、以下のデータが含まれている必要があります。
  * メソッド・タイプ - この場合、POST (大文字)
  * コンテンツ・タイプ - "Content-Type" ヘッダー内で見つかります
  * ペイロード - 要求本文。 この例では、JSON ストリングが、ネイティブの連想配列またはディクショナリーにデコードされていると想定しています。  
  * nonce - "「X-IBM-Nonce」" ヘッダー内で見つかります

  正規ストリングを作成するには、正規ストリング・データを、以下の正確な順序で、区切り文字なしで結合します。

  メソッド・タイプ + コンテンツ・タイプ+ ペイロード['id'] + ペイロード['serviceName'] + ペイロード['event'] + ペイロード['time stamp'] + Nonce

2. 正規ストリングをハッシュします。

  一時仮想サーバー Web フックで使用されるハッシュ・アルゴリズムは、鍵付きハッシュ・アルゴリズムである HMAC-SHA256 です。 使用される鍵は、Web フックがセットアップされたときに指定された secret です。

3. ハッシュされた正規ストリングを Base64 にエンコードします。

4. 結果のストリングを 'Authorization' ヘッダー内の署名と比較します。  

  タイミング攻撃に対して安全なストリング比較関数を使用してください。 ストリングが一致しない場合、要求を受け入れないでください。

## `reclaim-scheduled` 通知要求ペイロードの構造

一時仮想サーバー Web フックから送信される要求は、ヘッダーとペイロードを含むという点で、HTTP 要求に似ています。 ペイロードは、以下の形式の JSON フォーマットのストリングです。

**注**: キー名がこの特定の順序になるという保証はありません。

	{
		'event': 'reclaim-scheduled',
		'id': <string - that is the ID of the transient guest being reclaimed>,
		'link': <string - link for an API call to return info about the guest being reaped>,
		'serviceName': <string - name of the API service class>,
		'time stamp': <integer - timestamp of when the reclaim was scheduled>
	}


## HMAC 署名を作成するためのコードの例

Python:

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

PHP:

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

Node.js:

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
