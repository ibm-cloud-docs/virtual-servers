---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-22"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 専用ホストの価格設定
{: #dedicated-virtual-server-pricing}

専用ホストの価格設定は、時間単位および月単位のモデルで提供されます。
{:shortdesc}

専用ホストの価格設定には、専用ホストにインスタンスがプロビジョンされたときのすべての vCPU、RAM、ローカル・ストレージ、アップリンク・ポート速度のコンポーネントが含まれます。価格設定について詳しくは、[Virtual servers provisioning calculator ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window} を参照してください。

専用ホストでは、1 番目、2 番目、3 番目、4 番目、5 番目のディスクで追加のローカル・ストレージ・ディスクを使用可能です。 また、各 2 次ディスクには最大 400 GB の追加容量があります。

時間単位のインスタンスは、時間単位と月単位のホストでプロビジョン可能です。 月単位のインスタンスは、月単位のホストでのみプロビジョンできます。

| ホスト構成 | vCPU	| RAM (GB) | ローカル・ストレージ (TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |  56 	|   242    |        	1.2	          |
| 56x484x1.2         |  56  |   484    |          1.2           |
{: caption="表 1. 専用ホストの構成" caption-side="top"}

価格設定は地域によって異なります。
{:note}

SAN (ネットワーク接続)、プレミアム OS、SW アドオンは、専用ホストにプロビジョンされたインスタンスに応じて、時間単位または月単位でインスタンス別に課金されます。これらのコンポーネントの価格設定は、パブリック・インスタンスおよび専用インスタンスでの既存オファリングと一貫しています。 

例えば、以下の構成で専用ホストにプロビジョンされる専用インスタンスは、インスタンス別には課金されません。vCPU、RAM、ローカル・ストレージ、およびアップリンク・ポート速度は、専用ホストの料金に含まれます。 

* 8 vCPU
* 16 GB RAM
* 100 GB ローカル SSD 1 番目のディスク
* 400 GB ローカル SSD 2 番目のディスク
* 400 GB ローカル SSD 3 番目のディスク
* 1 Gbps パブリック・ネットワークおよびプライベート・ネットワークのアップリンク (専用ホスト) 

