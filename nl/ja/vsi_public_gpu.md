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

# GPU
{: #gpu}

GPU プロファイルは、リソース管理とコストを削減するためにより高いコンピュート密度を必要とする高パフォーマンスのワークロードに最適です。GPU プロファイルは、人工知能処理、グラフィックとデータを大量に使用するアプリケーション、または高速なパフォーマンスを必要とする新規アプリケーションの開発に理想的です。

NVDIA Tesla GPU を採用した {{site.data.keyword.cloud_notm}} Accelerated Compute の「ac1」および「ac2」のフレーバーは両方ともブロック・ストレージとローカル SSD ストレージを提供しています。 以下の GPU プロファイルの中から選択できます。  

  <table>
<CAPTION>表 1. P100 GPU プロファイル</CAPTION>
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

**注:** P100 GPU プロファイルは、_DAL13_、_LON06_、および _WDC07_ のデータ・センターで使用可能です。

<table>
<CAPTION>表 2. V100 GPU プロファイル</CAPTION>
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

**注:** V100 GPU プロファイルは、_DAL10_、_DAL12_、_LON04_、および _WDC07_ のデータ・センターで使用可能です。


## 始めに
以下の GPU の前提条件を確認してください。

1. GPU プロファイルの仮想サーバーは、Hardware Virtual Machine (HVM) ブート・モードをサポートするオペレーティング・システムでのみ使用可能です。HVM ブート・モードをサポートするオペレーティング・システムについては、以下のリストを確認してください。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 適切な NVIDIA ドライバーとソフトウェアをインストールする必要があります。 ソフトウェアと NVIDIA ドライバーについて詳しくは、[GPU ドライバーおよびソフトウェア・パッケージのインストール](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages)を参照してください。  
**注:** インストールするソフトウェアには、前提ソフトウェアとオペレーティング・システム固有の構成がある可能性があります。

## GPU の追加または削除
最初の注文の後で、仮想サーバー上の GPU の数を変更することができます。 ただし、それは、プロビジョン済みの GPU の数によります。 次のいずれかのオプションがあります。

- プロビジョン済みの GPU が 1 つの場合、もう 1 つの GPU を追加できます。
- プロビジョン済みの GPU が 2 つの場合、1 つの GPU にフォールバックできます。
