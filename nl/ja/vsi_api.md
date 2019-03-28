---

copyright:
  years: 2017
lastupdated: "2017-10-25"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# API リファレンス
{: #api-reference}

{{site.data.keyword.slapi_full}} は、開発者やシステム管理者が {{site.data.keyword.cloud}} のバックエンド・システムと直接対話できるようにする開発用インターフェースです。 {{site.data.keyword.slapi_short}} により、{{site.data.keyword.slportal_full}}の多くの機能が使用可能になります。つまり、通常、{{site.data.keyword.slportal}}での操作が可能であれば、API でも実行することができます。 API 内で {{site.data.keyword.BluSoftlayer_full}} 環境のすべての部分とプログラムで対話できるため、{{site.data.keyword.slapi_short}} によってタスクを自動化できます。 例えば、*SoftLayer_Virtual_Guest/createObject* API を使用して、仮想サーバー・インスタンスをデプロイすることができます。
{:shortdesc}

{{site.data.keyword.slapi_short}} は、リモート・プロシージャー・コール・システムです。 各呼び出しには、API エンドポイントへのデータの送信と、それと引き換えに構造化データの受信が含まれます。 {{site.data.keyword.slapi_short}} を使用したデータの送受信に使用される形式は、選択した API 実装によって異なります。 {{site.data.keyword.slapi_short}} は現在、データ伝送に SOAP、XML-RPC、または REST を使用します。

{{site.data.keyword.slapi_short}} および仮想サーバー API について詳しくは、{{site.data.keyword.sldn_full}} の以下のリソースを参照してください。
* [{{site.data.keyword.slapi_short}} Overview ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/reference/softlayerapi/){: new_window}
* [Getting Started with the {{site.data.keyword.slapi_short}} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/article/getting-started/){: new_window}
* [API Reference: SoftLayer_Virtual_Guest::createObject ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/){: new_window}
* [API Reference: SoftLayer_Product_Order::placeOrder ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/){: new_window}

API の使用例については、以下の資料を参照してください。
* [Understanding and building an order using the {{site.data.keyword.slapi_short}} order CLI ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/article/understanding-ordering/){: new_window}
* [{{site.data.keyword.slapi_short}} Python Client: Working with Virtual Servers ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://softlayer-python.readthedocs.io/en/latest/cli/vs.html){: new_window}
* [{{site.data.keyword.slapi_short}} Examples - Release Notes ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/){: new_window}
* [Python サンプル ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/python/){: new_window}

## 専用仮想サーバーの使用例
* [Get Dedicated Host Allocation![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/python/getDediHostAllocation/){: new_window}
* [Get Dedicated Host Guests![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/python/getDedicatedHostGuests/){: new_window}
* [Migrate a virtual server instance between dedicated hosts![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/python/migrateDedicatedHost.py/){: new_window}

## パブリック仮想サーバーの使用例
* [softlayer_virtual_guest API サンプル![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/classes/softlayer_virtual_guest/){: new_window}
