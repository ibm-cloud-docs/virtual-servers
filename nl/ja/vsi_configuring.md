---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 仮想サーバーの構成
{: #configuring-virtual-servers}

仮想サーバーにアクセスしたら、必ずパスワードを変更してください。また、より安全な認証ソリューションとして SSH をセットアップすることを検討してください。環境のニーズに応じて仮想サーバーを構成できるように、さまざまなオプションがあります。
{:shortdesc}

## ログイン
アカウントを最初に作成したときに E メールで受け取った資格情報を使用して、[{{site.data.keyword.cloud}} コンソール ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://cloud.ibm.com/classic?){: new_window} にログインします。または、[{{site.data.keyword.slportal}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com/){:new_window} にログインできます。

## 仮想サーバーの検索
{{site.data.keyword.cloud_notm}} コンソールの「デバイス・リスト」で仮想サーバーを探します。 「デバイス・リスト」から、デバイスの管理、デバイスのアップグレード、帯域幅使用量グラフの生成を行えます。 詳しくは、[仮想サーバーの管理](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)を参照してください。

## パスワードの変更
強力なパスワード指針を使用してパスワードを変更します。[デバイスのユーザー名およびパスワードの表示と管理](/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device#view-update-user-name-password-for-device)を参照してください。

## SSH の構成
SSH はパスワード認証よりもセキュリティーの高いソリューションを提供します。[SSH 鍵入門](/docs/infrastructure/ssh-keys?topic=ssh-keys-getting-started-tutorial#getting-started-tutorial)を参照してください。

## IP アドレスと資格情報の記録
サーバーの IP アドレスと資格情報は、{{site.data.keyword.cloud_notm}} コンソールにログインしなくてもすぐに分かるように、記録して安全な場所に保管してください。
- 個別のデバイス IP アドレスは、「デバイス・リスト」から表示できます。
- 個別のデバイス・ルート・パスワードは、デバイスの「スナップショット」ビューから表示できます。 デバイス名の隣にある矢印をクリックして、表示を展開します。
- 複数のデバイス IP アドレスは、「デバイス・リスト」内の「CSV のダウンロード」アクションを使用して表示できます。 「設定」から「CSV のダウンロード」を選択して、デバイスと詳細の完全なリストをスプレッドシート形式でダウンロードします。

## ソフトウェアの資格情報の更新
プロビジョニング・プロセスでデバイスにロードされたソフトウェアにはすべて、一時的な資格情報が割り当てられています。 これらの資格情報は、{{site.data.keyword.cloud_notm}} コンソールの各デバイスの「パスワード」タブで表示および管理します。 この一時的な資格情報は、初めてソフトウェアにアクセスするときに使用します。 ベスト・プラクティスとして、初めてソフトウェアにアクセスした後にパスワードを変更してください。 文字、数字、記号を組み合わせた強力なパスワードを使用してください。

オプションで、各デバイスの「パスワード」タブにパスワード更新を保管できます。ただし、{{site.data.keyword.cloud_notm}} コンソール内にパスワードを保管すると、そのアカウントへのアクセス権と適切な許可を持つユーザーは誰でも「パスワード」画面に保管されたパスワードを表示できるようになることに注意してください。

ソフトウェアの資格情報の表示と管理について詳しくは、[クラシック・インフラストラクチャー・アクセス権限の管理](/docs/vsi?topic=iam-mngclassicinfra)を参照してください。

## プライベート・ネットワーク上のサーバーにアクセス
プライベート・ネットワークは、SSH と IP を介した KVM を使用してリモート・デスクトップ (RDP) 経由でお客様のデバイスと対話するための先駆となるものです。 VPN アクセス・ツールにより、最も近い SSL VPN エンドポイント、またはお客様が選択されるエンドポイントへのプライベート・ネットワーク接続が可能になります。 VPN アクセスは、いくつかの提供サービスと対話するためにも必要です。 詳しくは、[仮想プライベート・ネットワーキング (VPN) の概説 (Getting started with Virtual Private Networking (VPN)) ](/docs/infrastructure/iaas-vpn?topic=VPN-gettingstarted-with-virtual-private-networking)を参照してください。

## モニタリングのセットアップ
モニタリングは主にサーバーのアップタイムを確認するためのリソースとして使用されますが、拡張すべき時期を確認するためにも役立ちます。 さまざまなモニタリング・ニーズに対応するために、標準モニタリングと Nimsoft モニタリングの両方のサービスが利用可能です。 標準モニタリングは、「基本モニタリング」とも呼ばれ、一般に、{{site.data.keyword.cloud_notm}} コンソールを使用して開始される低速または保守の ping を使用する ping と応答の方式で使用されます。 Nimsoft モニタリングは、「拡張モニタリング」とも呼ばれ、Basic、Advanced、Premium の 3 つの層で提供されています。 このサービスは {{site.data.keyword.cloud_notm}} コンソール経由でもアクセスできます。 詳しくは、[モニタリング (Monitoring) ](/docs/infrastructure/SLmonitoring?topic=slmonitoring-monitoring#monitoring)を参照してください。

## セキュリティー・グループの構成
セキュリティー・グループを使用して仮想サーバーのネットワーク・トラフィックを制限することができます。セキュリティー・グループを使用すると、仮想サーバー・インスタンスのパブリック・インターフェースとプライベート・インターフェースの両方に、入出力トラフィックの処理方法を定義する一連の IP フィルター・ルールを設定できます。
詳しくは、[セキュリティー・グループの概説](/docs/infrastructure/security-groups?topic=security-groups-getting-started)を参照してください。

## ファイアウォールの構成
保護をより強化するために、ハードウェアのファイアウォールを使用することもできます。ハードウェアのファイアウォールは、ダウン時間を発生させずにオンデマンドでプロビジョンされます。 ルールが適切に確立されていれば、ファイアウォールによって、望ましくないアクティビティーからサーバーを保護できます。 ファイアウォールを注文した後、ファイアウォールを有効に設定して、ルールを設定する必要があります。

詳しくは、以下の情報を参照してください。

* [ハードウェア・ファイアウォール (共有)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [ハードウェア・ファイアウォール (専用)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)

## バックアップのスケジュール
バックアップにより、デバイスの外部でデータを確実に安全に保管でき、失われた場合にも保護できます。 デバイスに情報を再ロードする必要が生じた場合に備えて、データを安全な場所に保管するために、以下のバックアップ・サービスが利用可能です。
- {{site.data.keyword.backup_notm}}は、エージェント・ベースの自動バックアップ・システムです。 これは、「設定するだけ」の一般的なデバイス管理ソリューションです。 追加のプラグインを使用することで、Exchange や SQL などの Microsoft ソフトウェアと互換性があります。 {{site.data.keyword.backup_notm}}・ユーザーは、{{site.data.keyword.backup_notm}}の WebCC Web ベース・アプリケーションを通じてこのサービスと対話します。 詳しくは、[{{site.data.keyword.backup_notm}}・サービスの概説](/docs/infrastructure/Backup?topic=Backup-getting-started)を参照してください。
- R1Soft Continuous Data Protection は、ご使用のサーバーまたは自己管理型仮想マシンにインストールできるバックアップ・ソフトウェアです。 すべてのバックアップを管理するための単一のインターフェースが必要な場合にお勧めします。 R1Soft CDP の操作は専有管理システムを使用して行います。これは、エージェントを仮想マシンにインストールできるようにし、追加機能のデータベース・プラグインを提供します。 詳しくは、[{{site.data.keyword.backup_notm}}・サービスの概説](/docs/infrastructure/Backup?topic=Backup-getting-started)を参照してください。

## 次のステップ
仮想サーバーが構成されたら、その管理を開始できます。 詳しくは、[仮想サーバーの管理](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)を参照してください。
