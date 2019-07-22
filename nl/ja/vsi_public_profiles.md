---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

keywords: public virtual servers, network traffic, virtual server deployment, profile

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# プロファイル
{: #about-virtual-server-profiles}

{{site.data.keyword.cloud}} 仮想サーバー・インスタンスをプロビジョンするときには、サポートされているプロファイル・ファミリーの中から選択することができます。プロファイルとは、vCPU と RAM の組み合わせです。プロファイルをインスタンス化することで、すぐに仮想サーバー・インスタンスを開始できます。 {{site.data.keyword.cloud_notm}} コンソールで、一般的なプロファイル構成の中から選択するか、ニーズに最もよく合うプロファイルのリストから選択することができます。
{:shortdesc}

以下の仮想サーバー・インスタンス・ファミリーを使用できます。

インスタンスのタイプによっては使用できないファミリーもあります。
{:note}

| ファミリー  | 説明                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [平衡型](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | パフォーマンスとスケーラビリティーのバランスを必要とする、一般的なクラウド・ワークロードに最適です。 Network Attached Storage を使用します。 |
| [平衡型ローカル・ストレージ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | 非常に低遅延で高い入出力性能を必要とする大きなデータベース・ワークロードに最適です。|
| [コンピュート](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | 中規模から大規模の Web トラフィック・ワークロードに最適です。 |
| [メモリー](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | メモリー・キャッシュおよびリアルタイム分析ワークロードに最適です。 |
| [GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  | 高パフォーマンスのワークロードに最適です。 |
{: caption="表 1. パブリック仮想サーバー・ファミリーの選択" caption-side="top"}

これらのファミリーの中には、VPC 用の IBM Cloud Virtual Servers でも使用可能なものがあります。 詳しくは、[
仮想プライベート・クラウド用の IBM Virtual Servers](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen)を参照してください。
{:tip}

## 平衡型
{: #balanced}

平衡型プロファイル (Network Attached Storage を使用) は、パフォーマンスとスケーリングのバランスを必要とする一般的なクラウド・ワークロードに適しています。ネットワーク・パフォーマンスは、標準からプレミアムまで多岐にわたります。

このオファリングは、以下のプロファイルで利用可能です。

| プロファイル   | vCPU    | RAM     | ストレージ・タイプ |
| --------- | ------- | ------- | ------------ |
| B1.1x2    | 1       | 2 GB    | SAN          |
| B1.1x4    | 1       | 4 GB    | SAN          |
| B1.2x4    | 2       | 4 GB    | SAN          |
| B1.2x8    | 2       | 8 GB    | SAN          |
| B1.4x8    | 4       | 8 GB    | SAN          |
| B1.4x16   | 4       | 16 GB   | SAN          |
| B1.8x16   | 8       | 16 GB   | SAN          |
| B1.8x32   | 8       | 32 GB   | SAN          |
| B1.16x32  | 16      | 32 GB   | SAN          |
| B1.16x64  | 16      | 64 GB   | SAN          |
| B1.32x64  | 32      | 64 GB   | SAN          |
| B1.32x128 | 32      | 128 GB  | SAN          |
| B1.48x192 | 48      | 192 GB  | SAN          |
{: caption="表 2. 平衡型プロファイル (Network Attached Storage を使用)" caption-side="top"}

### ストレージの注

* SAN 1 次ブート・ディスク (25 GB または 100 GB) で、それぞれ 2 TB までの追加ディスクが使用可能 (合計 5 個のディスクが許可される)。
* SAN ストレージを使用するパブリック仮想サーバーの料金には、仮想 CPU、メモリー、および最小 1 次ブート・ディスクが含まれます。 追加のディスクの価格は、選択するディスクのサイズと数量で決まります。  

平衡型プロファイル (Network Attached Storage を使用) は、すべてのデータ・センターで使用可能です。

すべてのサポート対象オペレーティング・システム (RHEL、CentOS、Windows、Ubuntu、およびその他)、サポート対象データベース、およびソフトウェア・アドオンもこのオファリングで使用可能です。 

## 平衡型ローカル・ストレージ
{: #balanced-local-storage}

 平衡型ローカル・ストレージ・プロファイルは、主に、非常に低遅延で高い入出力性能を必要とする大きなデータベース・ワークロードを対象としています。ネットワーク・パフォーマンスは、標準からプレミアムまで多岐にわたります。

このオファリングは各種のプロファイルおよびデータ・センターで提供されており、以下のローカル・ストレージ・オプションがあります。

* [ローカル HDD](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [ローカル SSD](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### ローカル HDD
{: #HDD}
 
<table>
<CAPTION>表 3. ローカル HDD を使用した平衡型ローカル・ストレージ・プロファイル</CAPTION>
<THEAD>
<TR>
<th>プロファイル</th>
<th>vCPU</th>
<th>RAM</th>
<th>2 次ディスク<sup>(*)</sup></th>
<th>ストレージ・タイプ</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25、100 GB</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25、100 GB</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100、200 GB</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100、200 GB</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150、300 GB</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150、300 GB</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>ローカル HDD</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>ローカル HDD</td>
</tr>
</TBODY>
</table>

#### ストレージの注
* <sup>(*)</sup>平衡型ローカル・プロファイルには、自動的に、100 GB のローカル・ストレージ・ブート・ディスクが付属します。 ユーザーは、2 番目のディスク (表 3 に示されたオプション) を選択できます。 追加のローカル・ディスクはすべてオプションです。 必要量が 500 GB を超える場合は、2 つの追加ディスクが必要になります (例えば、8 コアには、2 x 250 GB のローカル・ストレージが必要)。
*	最大ローカル・ストレージは、コアによって制限されます。 
*	平衡型ローカル・ストレージはグローバルに使用可能ですが、ストレージのタイプ (ローカル SSD またはローカル HDD) は、データ・センターの場所によって異なります。 
*	1 次ディスクも 2 次ディスクも切り離すことはできません。

以下のデータ・センターは、ローカル HDD を使用した平衡型ローカル・ストレージ仮想サーバーをサポートしています。

| 使用可能なデータ・センター - ローカル HDD |       |
| ---------------------- | ----- |
| ダラス (DAL01)         | ダラス (DAL05)   |
| ダラス (DAL06)         | ヒューストン (HOU02)  |
| シアトル (SEA01)        | サンノゼ (SJC01) |
| ワシントン、DC (WDC01) |                  |
{: class="simple-tab-table"}
{: caption="表 4. 使用可能なデータ・センター (ローカル HDD) - アメリカ大陸" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| 使用可能なデータ・センター - ローカル HDD |
| ---------------------- |
| アムステルダム (AMS01)      |
{: class="simple-tab-table"}
{: caption="表 5. 使用可能なデータ・センター (ローカル HDD) - ヨーロッパ" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| 使用可能なデータ・センター - ローカル HDD |
| ---------------------- |
| ホンコン (HKG02)      | 
| シンガポール (SNG01)      |
{: class="simple-tab-table"}
{: caption="表 6. 使用可能なデータ・センター (ローカル HDD) - アジア太平洋" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

すべてのサポート対象オペレーティング・システム (RHEL、CentOS、Windows、Ubuntu、およびその他)、サポート対象データベース、およびソフトウェア・アドオンもこのオファリングで使用可能です。  

### ローカル SSD 
{: #SSD}

<table>
<CAPTION>表 7. ローカル SSD を使用した平衡型ローカル・ストレージ・プロファイル</CAPTION>
<THEAD>
<TR>
<th>プロファイル</th>
<th>vCPU</th>
<th>RAM</th>
<th>2 次ディスク<sup>(*)</sup></th>
<th>ストレージ・タイプ</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25、100 GB</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25、100 GB</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100、200 GB</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100、200 GB</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150、300 GB</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150、300 GB</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB、(2 x 250 GB)</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB、(2 x 300 GB)</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>ローカル SSD</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB、(2 x 400 GB)</td>
<td>ローカル SSD</td>
</tr>
</TBODY>
</table>

#### ストレージの注
* <sup>(*)</sup>平衡型ローカル・プロファイルには、自動的に、100 GB のローカル・ストレージ・ブート・ディスクが付属します。 ユーザーは、2 番目のディスク (上記の表に示されたオプション) を選択できます。 追加のローカル・ディスクはすべてオプションです。 必要量が 500 GB を超える場合は、2 つの追加ディスクが必要になります (例えば、8 コアには、2 x 250 GB のローカル・ストレージが必要)。
*	最大ローカル・ストレージは、コアによって制限されます。 
*	平衡型ローカル・ストレージはグローバルに使用可能ですが、ストレージのタイプ (ローカル SSD またはローカル HDD) は、データ・センターの場所によって異なります。 
*	1 次ディスクも 2 次ディスクも切り離すことはできません。

以下のデータ・センターは、ローカル SSD を使用した平衡型ローカル・ストレージ仮想サーバーをサポートしています。

| 使用可能なデータ・センター - ローカル SDD |        |
| ---------------------------------- | ------ |
| ダラス (DAL09)                     | ダラス (DAL10)         |
| ダラス (DAL12)                     | ダラス (DAL13)         |
| ケレタロ (MEX01)                  | モントリオール (MON01)       |
| サンパウロ (SAO01)                  | サンノゼ (SJC03)       |
| サンノゼ (SJC04)                   | トロント (TOR01)        |
| ワシントン、DC (WDC04)             | ワシントン、DC (WDC06) |
| ワシントン、DC (WDC07)             |                        |
{: class="simple-tab-table"}
{: caption="表 8. 使用可能なデータ・センター (ローカル SDD) - アメリカ大陸" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| 使用可能なデータ・センター - ローカル SDD |       |
| ---------------------------------- | ----- |
| アムステルダム (AMS03)                  | フランクフルト (FRA02) |
| ロンドン (LON02)                     | ロンドン (LON04)    |
| ロンドン (LON06)                     | ミラノ (MIL01)     |
| オスロ (OSL01)                       | パリ (PAR01)     |
{: class="simple-tab-table"}
{: caption="表 9. 使用可能なデータ・センター (ローカル SDD) - ヨーロッパ" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| 使用可能なデータ・センター - ローカル SDD |       |
| ---------------------------------- | ----- |
| チェンナイ (CHE01)                    | メルボルン (MEL01) |
| ソウル (SEO01)                      | シドニー (SYD01)    |
| シドニー (SYD04)                     | 東京 (TOK02)     |
{: class="simple-tab-table"}
{: caption="表 10. 使用可能なデータ・センター (ローカル SDD) - アジア太平洋" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

すべてのサポート対象オペレーティング・システム (RHEL、CentOS、Windows、Ubuntu、およびその他)、サポート対象データベース、およびソフトウェア・アドオンもこのオファリングで使用可能です。

## コンピュート
{: #compute}

コンピュート・プロファイルは、Web トラフィックが多いワークロード、実動バッチ処理、およびフロントエンド Web サーバーなどの集中的 CPU デマンドがあるワークロードに最適です。

このオファリングは、以下のプロファイルで利用可能です。

| プロファイル      | vCPU     | RAM       | ストレージ・タイプ |
| ------------ | -------- | --------- | ------------ |
| C1.1x1       | 1        | 1 GB      | SAN          |
| C1.2x2       | 2        | 2 GB      | SAN          |
| C1.4x4       | 4        | 4 GB      | SAN          |
| C1.8x8       | 8        | 8 GB      | SAN          |
| C1.16x16     | 16       | 16 GB     | SAN          |
| C1.32x32     | 32       | 32 GB     | SAN          |
{: caption="表 11. コンピュート・プロファイル" caption-side="top"}

### ストレージの注
* SAN 1 次ブート・ディスク (25 GB または 100 GB) で、それぞれ 2 TB までの追加ディスクが使用可能 (合計 5 個のディスクが許可される)。
* SAN ストレージを使用するパブリック仮想サーバーの料金には、仮想 CPU、メモリー、および最小 1 次ブート・ディスクが含まれます。 追加のディスクの価格は、選択するディスクのサイズと数量で決まります。  

コンピュート・プロファイルは、すべてのデータ・センターで使用可能です。

すべてのサポート対象オペレーティング・システム (RHEL、CentOS、Windows、Ubuntu、およびその他)、サポート対象データベース、およびソフトウェア・アドオンもこのオファリングで使用可能です。

## メモリー
{: #memory}

メモリー・プロファイルは、キャッシング量が多いワークロード、集中型データベース・アプリケーション、またはメモリー内分析ワークロードなどのメモリー集中型ワークロードに最適です。

このオファリングは、以下のプロファイルで利用可能です。

| プロファイル      | vCPU     | RAM       | ストレージ・タイプ |
| ------------ | -------- | --------- | ------------ |
| M1.1x8       | 1        | 8 GB      | SAN          |
| M1.2x16      | 2        | 16 GB     | SAN          |
| M1.4x32      | 4        | 32 GB     | SAN          |
| M1.8x64      | 8        | 64 GB     | SAN          |
| M1.16x128    | 16       | 128 GB    | SAN          |
| M1.30x240    | 30       | 240 GB    | SAN          |
| M1.48x384    | 48       | 384 GB    | SAN          |
| M1.56x448    | 56       | 448 GB    | SAN          |
| M1.64x512    | 64       | 512 GB    | SAN          |
{: caption="表 12. メモリー・プロファイル" caption-side="top"}

### ストレージの注
* SAN 1 次ブート・ディスク (25 GB または 100 GB) で、それぞれ 2 TB までの追加ディスクが使用可能 (合計 5 個のディスクが許可される)。
* SAN ストレージを使用するパブリック仮想サーバーの料金には、仮想 CPU、メモリー、および最小 1 次ブート・ディスクが含まれます。 追加のディスクの価格は、選択するディスクのサイズと数量で決まります。  

メモリー・プロファイルは、すべてのデータ・センターで使用可能です。

すべてのサポート対象オペレーティング・システム (RHEL、CentOS、Windows、Ubuntu、およびその他)、サポート対象データベース、およびソフトウェア・アドオンもこのオファリングで使用可能です。

## GPU
{: #gpu}

GPU プロファイルは、リソース管理とコストを削減するためにより高いコンピュート密度を必要とする高パフォーマンスのワークロードに最適です。 GPU プロファイルは、人工知能処理、グラフィックとデータを大量に使用するアプリケーション、または高速なパフォーマンスを必要とする新規アプリケーションの開発に理想的です。

NVDIA Tesla GPU を採用した {{site.data.keyword.cloud_notm}} Accelerated Compute の「ac1」および「ac2」のプロファイルは両方ともブロック・ストレージとローカル SSD ストレージを提供しています。 以下の GPU プロファイルの中から選択できます。  

<table>
<CAPTION>表 13. P100 GPU プロファイル</CAPTION>
<THEAD>
<TR>
<th>プロファイル</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>ストレージ・タイプ</th>
<th>ブート・ディスク (GB)</th>
<th>2 次ディスク (2 および 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>ブロック (SAN)</td>
<td>25</td>
<td>なし</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>ローカル SSD または SAN</td>
<td>100</td>
<td>なし (SAN)<br>300 (ローカル)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>ブロック (SAN)</td>
<td>25</td>
<td>なし</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>ローカル SSD または SAN</td>
<td>100</td>
<td>なし (SAN)<br>600 (ローカル)</td></tr>

</TBODY>
</table>

P100 GPU プロファイルは、_DAL13_、_LON06_、および _WDC07_ のデータ・センターで使用可能です。
{: note}

<table>
<CAPTION>表 14. V100 GPU プロファイル</CAPTION>
<THEAD>
<TR>
<th>プロファイル</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>ストレージ・タイプ</th>
<th>ブート・ディスク (GB)</th>
<th>2 次ディスク (2 および 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>ブロック (SAN)</td>
<td>25</td>
<td>なし</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>ローカル SSD または SAN</td>
<td>100</td>
<td>なし (SAN)<br>300 (ローカル)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>ブロック (SAN)</td>
<td>25</td>
<td>なし</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>ローカル SSD または SAN</td>
<td>100</td>
<td>なし (SAN)<br>600 (ローカル)</td></tr>

</TBODY>
</table>

V100 GPU プロファイルは、_DAL10_、_DAL12_、_LON04_、および _WDC07_ のデータ・センターで使用可能です。
{: note}

### GPU の前提条件
以下の GPU の前提条件を確認してください。

1. GPU プロファイルの仮想サーバーは、Hardware Virtual Machine (HVM) ブート・モードをサポートするオペレーティング・システムでのみ使用可能です。 HVM ブート・モードをサポートするオペレーティング・システムについては、以下のリストを確認してください。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 適切な NVIDIA ドライバーとソフトウェアをインストールする必要があります。 ソフトウェアと NVIDIA ドライバーについて詳しくは、[GPU ドライバーおよびソフトウェア・パッケージのインストール](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages)を参照してください。  

インストールするソフトウェアには、前提ソフトウェアとオペレーティング・システム固有の構成がある可能性があります。
{: note}

### GPU の追加または削除 
最初の注文の後で、仮想サーバー上の GPU の数を変更することができます。 ただし、それは、プロビジョン済みの GPU の数によります。 次のいずれかのオプションがあります。

- プロビジョン済みの GPU が 1 つの場合、もう 1 つの GPU を追加できます。
- プロビジョン済みの GPU が 2 つの場合、1 つの GPU にフォールバックできます。

