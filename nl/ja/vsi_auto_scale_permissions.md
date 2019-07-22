---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# オート・スケールのユーザー権限のセットアップ
{: #user-permissions-required-to-use-auto-scale}

オート・スケール・オプションを利用するには、{{site.data.keyword.virtualmachinesshort}} を注文して管理する権限を超える特別なユーザー権限が必要です。オート・スケール機能を利用するためには、今後追加される仮想デバイスに加えて、アカウント上のすべての仮想サーバーを管理する権限が必要です。

アカウント管理者として、オート・スケール・オプションを利用する権限をユーザーに付与するには、以下の手順を実行します。

1. {{site.data.keyword.cloud}} コンソールの[「アクセス (IAM)」 ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://cloud.ibm.com/iam#/users){: new_window} ページにログインします。 
2. **「ユーザー」**タブで**「表示: クラシック・インフラストラクチャー・ユーザー (View by: My classic infrastructure users)」**を選択します。
3. ユーザーを選択してから**「クラシック・インフラストラクチャー」**タブをクリックします。
4. **「許可」タブ**の**「デバイス」**カテゴリーを展開し、**「自動スケーリング・グループの管理」**を選択します。
5. **「適用」**をクリックします。

## 次のステップ

オート・スケール・オプションにアクセスして使用する権限を取得したら、この機能を使用するための準備は完了です。最初に、以下の情報を検討してください。

1. [スケジュール・ベースのオート・スケールを使用したトラフィック・スパイクへの対処](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [リソース・ベースのオート・スケールを使用したトラフィック・スパイクへの対処](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [FAQ: オート・スケール](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

