---

copyright:
  years: 2018
lastupdated: "2018-08-01"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# サーバー IP アドレスの割り当て
{: #assigning-server-ip-addresses}

{{site.data.keyword.cloud}} は、プライベート・ネットワーク上の IPv4 アドレスを使用して仮想サーバー・インスタンスを構成し、要求された場合はパブリック (インターネットに向けた) IPv4 アドレスを使用して構成します。 さらに、パブリック・ネットワークの IPv6 アドレスを要求できます。 これらの IP アドレスはすべて、まとめて _1 次 IP アドレス_と呼ばれます。
{:shortdesc}

[{{site.data.keyword.slportal}} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://control.softlayer.com) を使用してセカンダリー・サブネットを購入した後、追加の IP アドレスを仮想サーバー・インスタンスにバインドできます。 この方法で購入して管理する IP アドレスは、_2 次 IP アドレス_と呼ばれます。

IP アドレスの取得に使用可能なオプションについて詳しくは、[サブネットおよび IP ](https://console.bluemix.net/docs/infrastructure/subnets/)を参照してください。

## 2 次 IP アドレスのバインディング

セカンダリー・サブネットを購入してルーティングしたら、新しく使用可能になった 1 つ以上の IP アドレスを使用するようにオペレーティング・システムを構成する必要があります。 新規 IP アドレスの構成ステップはオペレーティング・システムごとに異なりますが、このセットアップは通常、「インターフェース別名」のセットアップと呼ばれます。 追加の構成詳細情報については、ご使用のオペレーティング・システムの資料を参照してください。
