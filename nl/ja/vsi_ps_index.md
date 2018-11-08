---
copyright:
  years: 2014, 2018
lastupdated: "2018-10-18"
---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# プロビジョニング・スクリプト

プロビジョニング・スクリプトとは、プロビジョン処理中にデバイスにダウンロードされるか、または、デバイスにダウンロードされてから実行されるスクリプトです。 既存のアカウントの場合、プロビジョニング・スクリプトは {{site.data.keyword.slportal_full}} 内で管理されます。 注文処理中に、新規アカウント用のスクリプト、または、まだトラッキングされていないスクリプトを手動で入力できます。

あるいは、cloud-init 対応イメージを使用して、構成タスクを自動的に実行したりスクリプトを実行したりするためのユーザー・データを提供できます。詳しくは、[cloud-init 対応イメージを使用したプロビジョニング](/docs/infrastructure/image-templates/image_cloud-init.html#provisioning-with-a-cloud-init-enabled-image)を参照してください。
{: tip}

HTTP URL と関連付けられたプロビジョニング・スクリプトは、プロビジョニング処理中にデバイスにダウンロードされます。プロビジョン後、管理者がデバイス上でスクリプトを手動で実行する必要があります。 HTTPS URL と関連付けられたスクリプトは、ダウンロードされ、自動的に実行されます。 現在のところ、プロビジョニング・スクリプトは、標準 Linux オペレーティング・システム (Cent、RHEL、Fedora、Debian、または Ubuntu)、Windows、および FreeBSD で使用可能です。 その他のシステム (Vyatta、Netscaler、XenServer、VMware など) はサポートされていません。 プロビジョニング・スクリプトは、バイナリー・ファイルの組み合わせや任意の OS サポート言語など、オペレーティング・システムによって実行される任意のタイプのファイルであることが可能です。

詳しくは、[プロビジョニング・スクリプトの管理](add-provisioning-script.html)を参照してください。
