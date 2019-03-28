---

copyright:
  years: 2017
lastupdated: "2017-08-23"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# ファイアウォール
{: #virtual-server-security-options}

{{site.data.keyword.BluVirtServers}} には、不可欠なセキュリティー・レイヤーを提供するいくつかのファイアウォール・オプションがあります。  それらのファイアウォール・オプションは、サービスを中断せずに、オンデマンドでプロビジョンされます。 ファイアウォール・サービスは、不必要なトラフィックがサーバーに到達しないようにして、攻撃の可能性を減らし、意図した使用目的専用にサーバー・リソースを使用できるようにします。
{:shortdesc}

ファイアウォールは、Infrastructure パブリック・ネットワーク上のすべてのサーバーでアドオン機能として使用可能です。

オーダー・プロセスの一部として、デバイス固有のハードウェア・ファイアウォールまたはソフトウェア・ファイアウォールを選択して保護を提供することができます。 あるいは、専用のファイアウォール・アプライアンスを環境にデプロイし、保護された VLAN に仮想サーバーをデプロイすることもできます。  

**注:** 同じインターフェース上の 2 つのファイアウォール・アプライアンスによって仮想サーバーを保護することはできません。

詳しくは、以下のセキュリティーに関するトピックのコレクションを参照してください。

* [ハードウェア・ファイアウォール (共有)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-getting-started-with-hardware-firewall-shared)
* [ハードウェア・ファイアウォール (専用)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-getting-started-with-hardware-firewall-dedicated)
