---



copyright:
  years: 2017, 2018
lastupdated: "2018-2-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU フレーバーは、リソース管理とコストを削減するためにより高いコンピュート密度を必要とする高性能のワークロードに最適です。GPU は、グラフィックとデータを大量に使用するアプリケーション、または高速なパフォーマンスを必要とする新規アプリケーションの開発に理想的です。

NVDIA Tesla P100 GPU を採用した {{site.data.keyword.cloud_notm}} Accelerated Compute「ac1」ファミリーは、ブロック (ac1) ストレージとローカル SSD ストレージ (acl1) の両方を提供しています。以下の GPU フレーバーの中から選択できます。  

<table>

<caption>表 1. GPU フレーバー</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">GPU フレーバー</th>
<tr>
  <th>ac1.8x60</th>
  <th>acl1.8x60</th>
  <th>ac1.16x120</th>
  <th>acl1.16x120</th>
</tr>
</thead>
<TBODY>
<tr>
  <th><b>GPU</b></th>
  <td>1 x P100</td>
  <td>1 x P100</td>
  <td>2 x P100</td>
  <td>2 x P100</td>
</tr>
<tr>
  <th><b>GPU RAM (GB)</b></th>
  <td>16</td>
  <td>16</td>
  <td>32</td>
  <td>32</td>
</tr>

<tr>
  <th><b>vCPU</b></th>
  <td>8</td>
  <td>8</td>
  <td>16</td>
  <td>16</td>
</tr>

<tr>
  <th><b>vCPU RAM (GB)</b></th>
  <td>60</td>
  <td>60</td>
  <td>120</td>
  <td>120</td>
</tr>

<tr>
  <th><b>ストレージ・タイプ</b></th>
  <td>ブロック (SAN)</td>
  <td>ローカル SSD</td>
  <td>ブロック (SAN)</td>
  <td>ローカル SSD</td>
</tr>

<tr>
  <th><b>ブート・ディスク (GB)</b></th>
  <td>25 および 100</td>
  <td>100</td>
  <td>25 および 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>2 次ディスク (GB)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**注:** GPU フレーバーは、_DAL13_ データ・センターで使用可能です。

## 始めに
以下の GPU の前提条件を確認してください。

1. GPU ファミリーの仮想サーバーは、Hardware Virtual Machine (HVM) ブート・モードをサポートするオペレーティング・システムでのみ使用可能です。HVM ブート・モードをサポートするオペレーティング・システムについては、以下のリストを確認してください。  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. 適切な NVIDIA ドライバーとソフトウェアをインストールする必要があります。ソフトウェアと NVIDIA ドライバーについて詳しくは、[GPU ドライバーおよびソフトウェア・パッケージのインストール](../vsi/vsi_gpu_nvidia_drivers.html)を参照してください。

**注:** インストールするソフトウェアには、前提ソフトウェアとオペレーティング・システム固有の構成がある可能性があります。


