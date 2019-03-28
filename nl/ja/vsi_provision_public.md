---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-11"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# パブリック・インスタンスのプロビジョニング
{: #ordering-vs-public}

## 始めに
パブリック仮想サーバー・インスタンスをプロビジョンするには、2 つのオプションがあります。 1 つ目は {{site.data.keyword.Bluemix}} カタログを使用する方法で、2 つ目は {{site.data.keyword.slportal}}を使用する方法です。 カタログと{{site.data.keyword.slportal}}には、固有のログイン ID が必要です。 カタログのユーザー名とパスワードはポータルへのログインには使用できず、ポータルのユーザー名とパスワードはカタログのログインには使用できません。
{:shortdesc}

始めに、以下の前提条件を確認してください。

  1. {{site.data.keyword.Bluemix_notm}} カタログまたは{{site.data.keyword.slportal}}の資格情報をセットアップ済みであることを確認してください。

     **注:** {{site.data.keyword.Bluemix_notm}} カタログの場合、仮想サーバーを注文するには、アップグレードされたアカウントを持っている必要があります。 アカウントのアップグレードについて詳しくは、[IBM ID への切り替え](/docs/account?topic=account-unifyingaccounts#unifyingaccounts)を参照してください。

  2. 使用可能なデプロイメント・オプションをまだ確認していない場合、確認します。 詳しくは、[デプロイメント・オプション: パブリック仮想サーバー](/docs/vsi?topic=virtual-servers-about-public-virtual-servers)を参照してください。

  3. 仮想サーバー・インスタンスの容量に関する考慮事項を確認します。  詳しくは、[容量に関する考慮事項](/docs/vsi?topic=virtual-servers-capacity-considerations)を参照してください。

## パブリック仮想サーバー・インスタンスのプロビジョニング
{: #ordering-public-instance}

前提条件を完了したら、パブリック仮想サーバー・インスタンスのプロビジョンを開始できます。 パブリック・インスタンスは、{{site.data.keyword.cloud_notm}} カタログまたは {{site.data.keyword.slportal}} からプロビジョンできます。

### IBM Cloud カタログを使用したパブリック仮想サーバー・インスタンスのプロビジョニング
{{site.data.keyword.cloud_notm}} カタログを使用してパブリック仮想サーバー・インスタンスをプロビジョンするには、以下のステップを実行します。

  1. ユーザー固有の資格情報を使用して [{{site.data.keyword.cloud_notm}} カタログ ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://console.bluemix.net/catalog/){: new_window} にログインします。
  2. **「コンピュート・インフラストラクチャー」**セクションで、**「仮想サーバー」**タイルをクリックします。
  3. **「パブリック仮想サーバー」**オプションを選択します。
  4. **「作成」**をクリックします。
  5. 仮想サーバー・インスタンスの関連情報をすべて入力します。
  6. オーダー要約を確認したら、**「サード・パーティー・サービス契約」**チェック・ボックスをクリックします。
  7. **「プロビジョン」**をクリックします。

### カスタマー・ポータルを使用したパブリック仮想サーバー・インスタンスのプロビジョニング
{{site.data.keyword.slportal}} を使用してパブリック仮想サーバー・インスタンスをプロビジョンするには、以下のステップを実行します。

  1. ユーザー固有の資格情報を使用して、[{{site.data.keyword.slportal}} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://control.softlayer.com/){: new_window} にログインします。
  2. **「オーダー」**セクションを見つけて、**「デバイス」**をクリックします。
  3. 「デバイス」ページで、仮想サーバー・オファリングのいずれかに対して**「時間単位 SAN  (Hourly SAN)」**、**「時間単位ローカル (Hourly local)」**、**「月単位 (Monthly)」**、または**「一時」**をクリックします。
  4. *「クラウド・サーバーの構成」*ページで、すべての関連情報を入力します。
  5. **「注文に追加」**ボタンをクリックして続行します。
  6. サーバーのドメイン情報を確認または編集します。
  7. **「クラウド・サービスのご利用条件」**チェック・ボックスと**「サード・パーティー・サービスのご使用条件」**チェック・ボックスをクリックします。
  8. 支払情報を確認または入力し、**「オーダーの送信」**ボタンをクリックします。 プロビジョニングのオーダー番号を含む画面にリダイレクトされます。 この画面は、プロビジョニングの注文の受信を示すものでもあるため、印刷できます。

 一連の E メール (プロビジョニング・オーダーの確認応答、プロビジョニング・オーダーの承認と処理、およびプロビジョニング完了) が管理者に送信されます。 プロビジョニング完了の E メールには、{{site.data.keyword.Bluemix_notm}} にログイン後の*「デバイスの詳細」* ページへのリンクが含まれています。 また、直接{{site.data.keyword.slportal}}にログインすることもできます。

## 次のステップ
仮想サーバーがプロビジョンされたら、その管理を開始できます。 詳しくは、[仮想サーバーの管理](/docs/vsi?topic=virtual-servers-managing-virtual-servers)を参照してください。
