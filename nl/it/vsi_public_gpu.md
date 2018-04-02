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
Le caratteristiche GPU sono migliori per i carichi di lavoro dalle prestazioni elevate che richiedono più densità di calcolo per ridurre la gestione delle risorse e i costi. I GPU sono ideali per le applicazioni di dati e grafiche intense o per lo sviluppo di nuove applicazioni che richiedono prestazioni veloci.

Con tecnologia NVDIA Tesla P100 GPUs, la famiglia {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” offre l'archiviazione blocchi (ac1) e SSD locale (acl1). Le seguenti caratteristiche GPU sono disponibili per la tua scelta:  

<table>

<caption>Tabella 1. Caratteristiche GPU</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">Caratteristiche GPU </th>
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
  <th><b>Tipo di archiviazione</b></th>
  <td>Blocchi (SAN)</td>
  <td>SSD locale</td>
  <td>Blocchi (SAN)</td>
  <td>SSD locale</td>
</tr>

<tr>
  <th><b>Disco di avvio (GB)</b></th>
  <td>25 e 100</td>
  <td>100</td>
  <td>25 e 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>Disc secondario (GB)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**Nota:** le caratteristiche GPU sono disponibili nel data center _DAL13_.

## Informazioni preliminari
Controlla i seguenti prerequisiti GPU.

1. I server virtuali della famiglia GPU sono disponibili solo su un sistema operativo che supporta la modalità di avvio HVM (Hardware Virtual Machine). Consulta il seguente elenco per i sistemi operativi con la modalità di avvio HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. Devono essere installati il software e i driver NVIDIA appropriati. Per ulteriori informazioni sul software e sui driver NVIDIA, consulta [Installazione dei driver GPU dai pacchetti software](../vsi/vsi_gpu_nvidia_drivers.html).

**Nota:** il software che istalli potrebbe avere del software prerequisito e delle configurazioni specifiche per sistema operativo.


