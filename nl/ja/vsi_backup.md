---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# バックアップ・サービス
{: #back-up-services}

## IBM Cloud バックアップ

{{site.data.keyword.backup_full}}は、{{site.data.keyword.backup_notm}} WebCC ブラウザー・ベースの管理ユーティリティーによって管理される、自動化されたエージェント・ベースのバックアップ・システムです。これは、{{site.data.keyword.BluSoftlayer}} ネットワーク上の 1 つ以上のデータ・センター内のサーバー間でデータをバックアップする方法をユーザーに提供します。管理者は、フル・システム、特定のディレクトリー、または個別のファイルをターゲットとする、毎時、日次、週次、またはカスタム・スケジュールで実行されるバックアップを設定できます。  追加のプラグインにより、Microsoft Exchange や Microsoft SQL のようなソフトウェアや、その他のタイプのサード・パーティー・ソフトウェアとの互換性が確保され、ユーザーは必要に応じてベア・メタルの復元を実行することができます。

{{site.data.keyword.backup_notm}}・サービスについて詳しくは、[{{site.data.keyword.backup_notm}}・サービスの概説](/docs/infrastructure/Backup?topic=Backup-gettingstarted#gettingstarted)を参照してください。


## R1Soft CDP

Continuous Data Protection (CDP) は、R1Soft によって作成された高性能バックアップ・ソフトウェアであり、物理デバイスと仮想デバイスの両方のバックアップに対応します。 Idera CDP は 3 つの主なコンポーネントで構成されます。つまり、CDP サーバー、エージェント、およびデータベース・プラグインです。データベース・プラグインは、最初の 2 つのコンポーネントとは別に購入できます。  R1Soft CDP はサード・パーティーのバックアップ・ソリューションであるため、CDP の操作は、{{site.data.keyword.Bluemix_short}} の専有インターフェースの完全に外側で行われます。ただし、R1Soft CDP のパスワードは、{{site.data.keyword.slportal}}内で追跡し、保管することができます。  R1Soft CDP の他の操作はすべて、R1Soft の Web サイトに記載されています。

R1Soft CDP バックアップ・サービスについて詳しくは、[R1Soft 資料 ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://wiki.r1soft.com/display/ServerBackupManager/Home){: new_window} を参照してください。
