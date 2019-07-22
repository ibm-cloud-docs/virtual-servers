---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-25"

keywords: reserved virtual servers, cost savings, guaranteed capacity 
subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 予約済み仮想サーバー
{: #about-reserved-virtual-servers}

{{site.data.keyword.BluVirtServers}}の予約済みインスタンス・オファリングは、将来のデプロイメントおよびコスト削減のために保証されたリソースが必要な場合に適しています。 予約済み容量の 1 年または 3 年の契約条件のいずれかを選択します。 その予約済み容量内で、特定のサイズの最大 20 個の仮想サーバー・インスタンスのセットを予約し、必要に応じてそれらのインスタンスをプロビジョンすることができます。 この容量は、契約条件の存続期間中、選択した POD およびデータ・センター内で保証されます。

予約済み仮想サーバー・インスタンスには、以下のような多くの利点があります。

* **保証された容量**

    容量を予約すると、契約条件の存続期間中その容量が保証されます。 
    
* **グローバル・アベイラビリティー**
    
    予約済み仮想サーバー・オファリングは、世界中のデータ・センターで利用可能です。

* **信頼できるプロビジョニング**
   
   仮想サーバー・インスタンスは、いつでも予約済み容量にプロビジョンおよび再利用できます。

* **コスト削減**
    
    1 年または 3 年間の契約期間を選択すると、毎月の支払い額を定額にでき、時間単位または月単位の仮想サーバーの請求サイクルと比べてコストを削減することができます。

予約済み仮想サーバー・インスタンスは、SAN バッキング・ストレージを使用するパブリック・インスタンスです。このオファリングでは、次のパブリック・インスタンス・ファミリーを利用できます。

| ファミリー  | 説明                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [平衡型](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | パフォーマンスとスケーラビリティーのバランスを必要とする、一般的なクラウド・ワークロードに最適です。 Network Attached Storage を使用します。|
| [コンピュート](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | 中型から大型の Web トラフィック・ワークロードに最適です。|
| [メモリー](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | メモリー・キャッシュおよびリアルタイム分析ワークロードに最適です。 |
{: caption="表 1. パブリック仮想サーバー・ファミリーの選択" caption-side="top"}

## 制限 

容量を予約し、予約済み仮想サーバー・インスタンスをプロビジョニングする前に、以下の制限を考慮してください。
  
  * インスタンスをアップグレードしたりダウングレードしたりすることはできません。
  * 予約済み容量は取り消せませんが、その容量内の仮想サーバー・インスタンスは再利用できます。
    
## 通知

予約済み仮想サーバーの容量の契約期間終了の 1 カ月前になると、E メール通知を受け取ります。

## 次のステップ

オプションを確認して決定したら、予約済み容量とインスタンスをプロビジョンします。 最初に、以下の情報を検討してください。

   1. [予約済み容量およびインスタンスのプロビジョニング](/docs/vsi?topic=virtual-servers-provisioning-reserved-capacity-and-instances#provisioning-reserved-capacity-and-instances)
   2. [FAQ: 予約済み容量およびインスタンス](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances)
