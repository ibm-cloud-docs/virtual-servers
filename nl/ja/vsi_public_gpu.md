---



copyright:
  years: 2017, 2018
lastupdated: "2018-6-18"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU フレーバーは、リソース管理とコストを削減するためにより高いコンピュート密度を必要とする高性能のワークロードに最適です。 GPU フレーバーは、グラフィックとデータを大量に使用するアプリケーション、または高速なパフォーマンスを必要とする新規アプリケーションの開発に理想的です。

NVDIA Tesla P100 GPU を採用した {{site.data.keyword.cloud_notm}} Accelerated Compute「ac1」フレーバーは、ブロック・ストレージとローカル SSD ストレージの両方を提供しています。以下の GPU フレーバーの中から選択できます。  

  <table>
<CAPTION>表 1. GPU フレーバー</CAPTION>
<THEAD>
<TR>
<th>フレーバー</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>ストレージ・タイプ</th>
<th>ブート・ディスク (GB)</th>
<th>2 次ディスク (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>ブロック (SAN)</td>
<td>25 および 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>ローカル SSD</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>ブロック (SAN)</td>
<td>25 および 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>ローカル SSD</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**注:** GPU フレーバーは、_DAL13_、_LON06_、および _WDC07_ のデータ・センターで使用可能です。

## 始めに
以下の GPU の前提条件を確認してください。

1. GPU フレーバーの仮想サーバーは、Hardware Virtual Machine (HVM) ブート・モードをサポートするオペレーティング・システムでのみ使用可能です。HVM ブート・モードをサポートするオペレーティング・システムについては、以下のリストを確認してください。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 適切な NVIDIA ドライバーとソフトウェアをインストールする必要があります。 ソフトウェアと NVIDIA ドライバーについて詳しくは、[GPU ドライバーおよびソフトウェア・パッケージのインストール](../vsi/vsi_gpu_nvidia_drivers.html)を参照してください。  
**注:** インストールするソフトウェアには、前提ソフトウェアとオペレーティング・システム固有の構成がある可能性があります。

# GPU の追加または削除
最初の注文の後で、仮想サーバー上の GPU の数を変更することができます。ただし、それは、プロビジョン済みの GPU の数によります。次のいずれかのオプションがあります。プロビジョニング注文画面では、以下のいずれかのオプションがあります。
- プロビジョン済みの GPU が 1 つの場合、もう 1 つの GPU を追加できます。
- プロビジョン済みの GPU が 2 つの場合、1 つの GPU にフォールバックできます。
