---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 専用インスタンスのプロビジョニング
{: #provisioning-dedicated-instances}

専用インスタンスをプロビジョンする方法には、2 つの選択肢があります。 1 つ目は {{site.data.keyword.Bluemix}} カタログを使用する方法で、2 つ目は {{site.data.keyword.slportal_full}}を使用する方法です。 カタログと{{site.data.keyword.slportal}}には、固有のログイン ID が必要です。 カタログのユーザー名とパスワードはポータルへのログインには使用できず、ポータルのユーザー名とパスワードはカタログのログインには使用できません。 {{site.data.keyword.Bluemix_notm}} カタログまたは {{site.data.keyword.slportal}} 資格情報をセットアップするには、[{{site.data.keyword.Bluemix_notm}} への登録](/docs/account?topic=account-signup#signup)を参照してください。
{:shortdesc}

## 専用仮想サーバー・インスタンスのプロビジョニング
{: #provision-dedicated-instances}
専用仮想サーバー・インスタンスは、{{site.data.keyword.cloud_notm}} カタログまたは {{site.data.keyword.slportal}} を使用してプロビジョンできます。

### IBM Cloud カタログを使用した専用仮想サーバー・インスタンスのプロビジョニング
{{site.data.keyword.cloud_notm}} カタログを使用して専用仮想サーバー・インスタンスをプロビジョンするには、以下のステップを実行します。

  1. ユーザー固有の資格情報を使用して [{{site.data.keyword.cloud_notm}} カタログ ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://console.bluemix.net/catalog/){: new_window} にログインします。
  2. **「コンピュート・インフラストラクチャー」**セクションで、**「仮想サーバー」**タイルをクリックします。
  3. **「専用仮想サーバー (Dedicated Virtual Server)」**オプションを選択します。
  4. **「作成」**をクリックします。
  5. **「専用ホスト」** セクションで、**「自動割り当て」**を選択します。 {{site.data.keyword.cloud_notm}} によって、選択したデータ・センター内のホストにインスタンスが自動的に割り当てられます。

     **注**: 専用ホストの場合は、**「ホストの指定」** または **「ホストの作成」**を選択します。 専用ホストおよび専用ホスト・インスタンスについて詳しくは、[専用仮想サーバー](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)を参照してください。

  5. 専用仮想サーバー・インスタンスに関連するすべての情報を入力します。
  6. オーダー要約を確認したら、**「サード・パーティー・サービス契約」**チェック・ボックスをクリックします。
  7. **「プロビジョン」**をクリックします。

### カスタマー・ポータルを使用した専用仮想サーバー・インスタンスのプロビジョニング
{{site.data.keyword.slportal}} を使用して専用仮想サーバー・インスタンスをプロビジョンするには、以下のステップを実行します。

1. ユーザー固有の資格情報を使用して、[{{site.data.keyword.slportal}} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://control.softlayer.com/){: new_window} にログインします。
2. **「オーダー」**セクションを見つけて、**「デバイス」**をクリックします。 **「SoftLayer 製品およびサービスの注文 (Order SoftLayer Product and Services)」**ウィンドウが表示されます。
3.  「Dedicated Virtual Servers」の下で、**「時間単位」**または**「月単位」**を選択します。 *「クラウド・サーバーの構成」* ページにリダイレクトされます。

4.	次の情報を入力します。

    <table>
    <CAPTION>表 1. 専用ホスト・インスタンスの選択</CAPTION>
    <THEAD>
    <TR>
    <th>フィールド</th>
    <th>値</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>数量</td>
    <td>デプロイする専用インスタンスの数。</td>
    </tr>
    <tr>
    <td>配置</td>
    <td>
    <ul>
    <li>自動割り当て – 選択したデータ・センター内のホストに、{{site.data.keyword.Bluemix_notm}} がインスタンスを自動的に割り当てます。</li>
    <li>ホストの指定 – 専用ホスト・インスタンスで使用されます。 専用ホストと専用ホスト・インスタンスについて詳しくは、[専用仮想サーバー](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers)を参照してください。</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>データ・センター</td>
    <td>インスタンスがプロビジョンされるデータ・センターを選択します。</td>
    </tr>
    <tr>
    <td>コンピューティング・インスタンス</td>
    <td> プロビジョニングの注文内の各インスタンスについて、メモリーと CPU を選択します。</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td> プロビジョニングの注文内の各インスタンスについて、RAM を選択します。</td>
    </tr>
    <tr>
    <td>オペレーティング・システム</td>
    <td>インスタンスのオペレーティング・システムを選択します。 サーバーとオペレーティング・システムの間で矛盾がある場合、エラー・メッセージが発行されます。 例えば、Microsoft SQL Server で Linux を選択する場合です。</td>
    </tr>
    <tr>
    <td>1 番目のディスク</td>
    <td>注文内の各インスタンスについて、「SAN」または「ローカル」を選択します。</td>
    </tr>
    <tr>
    <td>追加のディスク</td>
    <td>専用インスタンス当たり、最大 4 台の追加ブート・ディスク (SAN またはローカル) をプロビジョンできます。</td>
    </tr>
    <td>ネットワーク・オプション</td>
    <td> 該当のオプションを選択するか、デフォルト値を使用します。</td>
    </tr>
    <tr>
    <td>アドオン</td>
    <td> 該当のオプションを選択するか、デフォルト値を使用します。</td>
    </tr>
    <tr>
    </TBODY>
    </table>

5.	**「注文に追加」**ボタンをクリックします。 「清算」ページにリダイレクトされます。
6.  *「清算」*ページで*「拡張システム構成」* の下に、次の情報を入力します。

    <table>
    <CAPTION>表 2. 専用インスタンスの拡張システム構成</CAPTION>
    <THEAD>
    <TR>
    <th>フィールド</th>
    <th>値</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>VLAN の選択</td>
    <td>少なくとも 1 台のサーバーを注文済みの場合は、ご使用のアカウントで VLAN に新しいサーバーを追加します。</td>
    </tr>
    <tr>
    <td>プロビジョン・スクリプト</td>
    <td>プロビジョニング後の一定のステップを自動化できるスクリプトを指定します。</td>
    </tr>
    <tr>
    <td>SSH 鍵</td>
    <td>SSH 鍵の公開鍵を指定します。これにより、サーバーのプロビジョン後にサーバーにログインできます。</td>
    </tr>
    <tr>
    <td>ユーザー・メタデータ</td>
    <td>カスタム・プロビジョニング・スクリプトのオプション・メタデータ。</td>
    </tr>
    <tr>
    <td>ホスト名</td>
    <td>サーバーの永続的または一時的な名前を入力します。例えば、server1 などです。</td>
    </tr>
    <tr>
    <td>ドメイン</td>
    <td>インターネットのドメイン名と競合しないサブドメイン名を入力します。例えば、test.acme.com などです。</td>
    </tr>
    </TBODY>
    </table>

7.  **「クラウド・サービスのご利用条件」**と**「サード・パーティー・サービス契約」**のチェック・ボックスをクリックします。
8. 支払情報を確認または入力し、**「オーダーの送信」**ボタンをクリックします。 プロビジョニング注文番号が示された画面にリダイレクトされます。 この画面は、プロビジョニングの注文の受信を示すものでもあるため、印刷できます。

    プロビジョニング注文の確認、プロビジョニング注文の承認と処理、プロビジョニングの完了を示す一連の E メールが管理者に送信されます。 プロビジョニング完了 E メールには、{{site.data.keyword.Bluemix_notm}} へのログイン後に**「デバイスの詳細」**ページに直接移動するためのリンクが含まれています。 もう 1 つの選択肢として、{{site.data.keyword.slportal}}への直接ログインがあります。

## 次のステップ
仮想サーバーがプロビジョンされて使用可能になったら、{{site.data.keyword.slportal_full}}または {{site.data.keyword.slapi_full}} を使用して仮想サーバーを構成できます。 詳しくは、[仮想サーバーの構成](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers)を参照してください。
