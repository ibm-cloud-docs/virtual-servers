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

# 임시 가상 서버 재확보에 대한 알림 구성

임시 가상 서버는 본질적으로 오래 가지 않으며 언제든지 종료될 수 있고, 이는 데이터 손실로 이어질 수 있습니다. 자동화된 재확보 알림은 데이터 손실을 줄이는 데 도움을 줍니다. 임시 가상 서버는 프로비저닝될 때 실제 종료 전에 종료되기까지 **2분** 남았음을 알리는 알림을 수신하도록 구성될 수 있습니다. 알림을 통해 사용자는 임시 가상 서버에 진행 중인 처리를 완료하거나 필요한 데이터를 임시 가상 서버에서 전송하도록 프로그래밍 방식으로 경보를 보낼 수 있습니다. 

`reclaim-scheduled` 알림은 웹훅이며, 이는 알림이 HTTP POST 요청에 의해 사용자 제공 엔드포인트로 전송됨을 의미합니다. 이 웹훅을 설정하고 사용하려면 다음 단계를 완료하십시오.

1. 임시 가상 서버 인스턴스를 프로비저닝하십시오.
2. 웹훅을 설정하십시오.
3. 웹훅 요청을 확인하십시오.

## 임시 가상 서버 인스턴스 프로비저닝

임시 가상 서버는 [{{site.data.keyword.slportal_full}} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com/){: new_window} 또는 [SLDN API ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://sldn.softlayer.com){: new_window}를 통해 프로비저닝될 수 있습니다. 자세한 정보는 [임시 인스턴스 프로비저닝](/docs/vsi/vsi_provision_transient.html)을 참조하십시오.

## 웹훅 설정

웹훅을 설정하려면 SLDN API를 사용하여 임시 가상 서버 인스턴스에 다음 매개변수를 지정해야 합니다.

   * **URI** - `reclaim-scheduled` 알림이 전송되는 유효한 HTTP URI입니다.
   * **시크릿** - 요청에 서명하는 데 필요한 해시 알고리즘의 키로 사용되는 문자열입니다. 다른 사용자에게 시크릿 문자열을 알려주지 마십시오.

웹훅은 프로비저닝된 각 임시 가상 서버에 대해 설정해야 합니다. 그러나 URI 및 시크릿은 고유하지 않아도 됩니다.

두 매개변수는 모두 필수입니다. URI 또는 시크릿을 변경해야 하는 경우에는 새 정보로 메소드를 다시 호출하십시오.
{: tip}

임시 가상 서버 웹훅은 다음 메소드를 사용하여 SLDN API를 통해 설정할 수 있습니다.

  `SoftLayer_Virtual_Guest::setWebhook(uri, secret)`

자세한 정보는 [웹훅 설정 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/setTransientWebhook/){: new_window}에 대한 SLDN API 메소드 문서를 참조하십시오.

### reclaim-scheduled 알림 취소

`reclaim-scheduled` 알림을 취소하려면 다음 SLDN API 메소드를 호출하십시오.

  `SoftLayer_Virtual_Guest::deleteWebhook()`

자세한 정보는 [알림 취소 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/deleteTransientWebhook/){: new_window}에 대한 SLDN API 메소드 문서를 참조하십시오.

## 웹훅 요청 확인

`reclaim-scheduled` 알림을 확인하려면 다음 항목을 검토하십시오.

1. 요청의 시간소인

   요청이 수신된 시간과 요청 헤더에 있는 시간소인을 비교하여 확인하십시오. 차이가 30초보다 큰 경우에는 요청을 승인하지 마십시오. 이 조치는 반복 공격을 방지하는 데 도움을 줄 수 있습니다.

2. 요청의 "X-IBM-Nonce" 헤더에 있는 난스(nonce)

   이 값은 요청이 전송될 때 무작위로 생성되는 문자열입니다. 사용자는 요청에 포함된 난스(nonce)와 비교하기 위해 이전에 수신한 난스(nonce)를 저장하도록 선택할 수 있습니다. 요청에 있는 난스(nonce)를 이전에 사용한 경우 요청을 승인하지 마십시오. 이 조치는 반복 공격을 방지하는 데 도움을 줄 수 있습니다.

3. 요청의 "Authorization" 헤더에 있는 해시 메시지 인증 코드(HMAC)

   이 값은 제공된 시크릿 문자열을 키로 사용하는 HMAC-SHA256 알고리즘을 사용하여 해시 처리된 후에 Base64로 인코딩되는 문자열입니다. 사용자는 문자열을 생성하고, 해시하고, Base64로 인코딩한 후 결과를 "Authorization" 헤더의 시그니처와 비교해야 합니다. 이들이 일치하지 않는 경우에는 요청을 승인하지 마십시오. HMAC 시그니처 작성에 대한 세부사항은 다음 섹션을 참조하십시오. 

### HMAC 시그니처 비교

요청의 "Authorization" 헤더에 있는 HAMC 시그니처를 확인하려면, 비교 문자열을 작성해야 합니다. 이 문자열을 작성하려면 다음 단계를 완료하십시오.

1. 기준 문자열을 작성하십시오.

  기준 문자열은 다음 데이터를 포함해야 합니다.
  * 메소드 유형 - 이 경우 POST(대문자여야 함)
  * 컨텐츠 유형 - "Content-Type" 헤더에 있음
  * 페이로드 - 요청의 본문입니다. 이 예에서는 JSON 문자열이 기본 연관 배열 또는 사전으로 디코딩되었다고 가정합니다.   
  * 난스(nonce) - "X-IBM-Nonce" 헤더에 있음

  기준 문자열을 작성하려면, 정확히 다음과 같은 순서로 구분 기호 없이 기준 문자열 데이터를 결합하십시오.

  메소드 유형 + 컨텐츠 유형 + 페이로드['id'] + 페이로드['serviceName'] + 페이로드['event'] + 페이로드['time stamp'] + 난스(Nonce)

2. 기준 문자열을 해시하십시오.

  임시 가상 서버 웹훅에 사용되는 해싱 알고리즘은 HMAC-SHA256이며 이는 키를 사용하는 해싱 알고리즘입니다. 사용할 키는 웹훅이 설정될 때 제공된 시크릿입니다.

3. 해시된 기준 문자열을 Base64로 인코딩하십시오.

4. 결과 문자열을 'Authorization' 헤더의 시그니처와 비교하십시오.  

  타이밍 공격으로부터 안전한 문자열 비교 함수를 사용하십시오. 두 문자열이 일치하지 않는 경우에는 요청을 승인하지 마십시오.

## `reclaim-scheduled` 알림 요청 페이로드의 구조

임시 가상 서버 웹훅에서 전송되는 요청은 HTTP 요청과 같으며 여기에는 헤더와 페이로드가 있습니다. 페이로드는 다음 양식의 JSON 형식 문자열입니다.

**참고**: 키 이름은 반드시 여기에 지정된 순서대로인 것은 아닙니다.

	{
		'event': 'reclaim-scheduled',
		'id': <string - that is the ID of the transient guest being reclaimed>,
		'link': <string - link for an API call to return info about the guest being reaped>,
		'serviceName': <string - name of the API service class>,
		'time stamp': <integer - timestamp of when the reclaim was scheduled>
	}


## HMAC 시그니처 작성에 대한 코드 예

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
