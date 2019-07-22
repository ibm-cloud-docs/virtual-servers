---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# 仮想サーバー・インスタンスのリソースに関する考慮事項
{: #capacity-considerations}

## 現象

仮想サーバーのプロビジョン時に、以下のエラー・メッセージが表示されることがあります。

```
要求を完了するために使用できる容量が不足しています。(There is insufficient capacity to complete the request.)
```
{:screen}

プロビジョニングが失敗した場合、その特定の要求内のすべての仮想サーバー・インスタンスが失敗します。
{:tip}

## 現象の理由

サービス要求を実行するために使用できるリソースがルーターまたはデータ・センターに十分にない場合にエラーが発生します。このエラーが表示される場合、多数の理由が考えられます。 リソース・アベイラビリティーは頻繁に変わるため、しばらく待ってから後で再試行してください。

## 修正方法

以下の方法を使用して、プロビジョンを再試行できます。

1. 別のルーターを指定してプロビジョンする。  
2. ルーターを指定せずにプロビジョンする。
3. 別のデータ・センター内でプロビジョンする。
4. より少ないインスタンスをプロビジョンする。
5. 複数のデータ・センターにプロビジョンして、インスタンスを分散させる。
6. より小さいサイズのインスタンスをプロビジョンする。
7. VSI ストレージを SAN から LOCAL または LOCAL から SAN に変更する。
