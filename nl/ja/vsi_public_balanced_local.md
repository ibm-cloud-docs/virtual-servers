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

# 平衡型ローカル・ストレージ
{: #balanced-local-storage}

平衡型ローカル・ストレージ・プロファイルは、主に、高い (つまり低遅延の) 入出力パフォーマンスが要求される、大規模なデータベース・クラスターを対象としています。 このオファリングでは、リソースがオーバーサブスクライブされないため、より高いハイパフォーマンスが提供されます。 ネットワーク・パフォーマンスは、標準からプレミアムまで多岐にわたります。

このオファリングは各種のプロファイルおよびデータ・センターで提供されており、以下のローカル・ストレージ・オプションがあります。

* [ローカル HDD](/docs/vsi?topic=virtual-servers-HDD#HDD)
* [ローカル SSD](/docs/vsi?topic=virtual-servers-SSD#SSD)

## ローカル HDD {: #HDD}

<table>
<CAPTION>表 1. ローカル HDD を使用した平衡型ローカル・ストレージ・プロファイル</CAPTION>
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

**ストレージの注:**
* <sup>(*)</sup>平衡型ローカル・プロファイルには、自動的に、100 GB のローカル・ストレージ・ブート・ディスクが付属します。ユーザーは、2 番目のディスク (上記の表に示されたオプション) を選択できます。 追加のローカル・ディスクはすべてオプションです。 必要量が 500 GB を超える場合は、2 つの追加ディスクが必要になります (例えば、8 コアには、2 x 250 GB のローカル・ストレージが必要)。
*	最大ローカル・ストレージは、コアによって制限されます。
*	平衡型ローカル・ストレージはグローバルに使用可能ですが、ストレージのタイプ (ローカル SSD またはローカル HDD) は、データ・センターの場所によって異なります。
*	1 次ディスクも 2 次ディスクも切り離すことはできません。

以下のデータ・センターは、ローカル HDD を使用した平衡型ローカル・ストレージ仮想サーバーをサポートしています。

|データ・センター (ローカル HDD) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   |
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="表 1. サポートされるデータ・センター (ローカル HDD)" caption-side="top"}

すべてのサポート対象オペレーティング・システム (RHEL、CentOS、Windows、Ubuntu、およびその他)、サポート対象データベース、およびソフトウェア・アドオンもこのオファリングで使用可能です。  

## ローカル SSD {: #SSD}
<table>
<CAPTION>表 1. ローカル SSD を使用した平衡型ローカル・ストレージ・プロファイル</CAPTION>
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

**ストレージの注:**
* <sup>(*)</sup>平衡型ローカル・プロファイルには、自動的に、100 GB のローカル・ストレージ・ブート・ディスクが付属します。ユーザーは、2 番目のディスク (上記の表に示されたオプション) を選択できます。 追加のローカル・ディスクはすべてオプションです。 必要量が 500 GB を超える場合は、2 つの追加ディスクが必要になります (例えば、8 コアには、2 x 250 GB のローカル・ストレージが必要)。
*	最大ローカル・ストレージは、コアによって制限されます。
*	平衡型ローカル・ストレージはグローバルに使用可能ですが、ストレージのタイプ (ローカル SSD またはローカル HDD) は、データ・センターの場所によって異なります。
*	1 次ディスクも 2 次ディスクも切り離すことはできません。

以下のデータ・センターは、ローカル SSD を使用した平衡型ローカル・ストレージ仮想サーバーをサポートしています。

|データ・センター (ローカル SSD) |        |         |
|------- |------  |------ |
|AMS03   |LON06   |SJC03  |
|CHE01   |MEL01   |SJC04  |
|DAL09   |MEX01   |SYD01  |
|DAL10   |MIL01   |SYD04  |
|DAL12   |MON01   |TOK02  |       
|DAL13   |OSL01   |TOR01  |
|FRA02   |PAR01   |WDC04  |
|LON02   |SAO01   |WDC06  |
|LON04   |SEO01   | WDC07 |
{: caption="表 2. サポートされるデータ・センター (ローカル SSD)" caption-side="top"}

すべてのサポート対象オペレーティング・システム (RHEL、CentOS、Windows、Ubuntu、およびその他)、サポート対象データベース、およびソフトウェア・アドオンもこのオファリングで使用可能です。  
