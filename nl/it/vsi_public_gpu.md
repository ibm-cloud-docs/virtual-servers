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
Le caratteristiche GPU sono migliori per i carichi di lavoro dalle prestazioni elevate che richiedono più densità di calcolo per ridurre la gestione delle risorse e i costi. Le caratteristiche GPU sono ideali per le applicazioni di dati e grafiche intense o per lo sviluppo di nuove applicazioni che richiedono prestazioni veloci. 

Con tecnologia NVDIA Tesla P100 GPUs, la caratteristica {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” offre l'archiviazione blocchi e SSD locale. Le seguenti caratteristiche GPU sono disponibili per la tua scelta:  

  <table>
<CAPTION>Tabella 1. Caratteristiche GPU</CAPTION>
<THEAD>
<TR>
<th>Caratteristica</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>Tipo di archiviazione</th>
<th>Disco di avvio (GB)</th>
<th>Disco secondario (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Blocchi (SAN)</td>
<td>25 e 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD locale</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Blocchi (SAN)</td>
<td>25 e 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD locale</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**Nota:** le caratteristiche GPU sono disponibili nei data center _DAL13_, _LON06_ e _WDC07_.

## Informazioni preliminari
Controlla i seguenti prerequisiti GPU.

1. I server virtuali della caratteristica GPU sono disponibili solo su un sistema operativo che supporta la modalità di avvio HVM (Hardware Virtual Machine). Consulta il seguente elenco per i sistemi operativi con la modalità di avvio HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Devono essere installati il software e i driver NVIDIA appropriati. Per ulteriori informazioni sul software e sui driver NVIDIA, consulta [Installazione dei driver GPU dai pacchetti software](../vsi/vsi_gpu_nvidia_drivers.html).  
**Nota:** il software che istalli potrebbe avere del software prerequisito e delle configurazioni specifiche per sistema operativo.

# Aggiungi o rimuovi GPU
Puoi modificare il numero di GPU sul tuo server virtuale dopo l'ordine iniziale. Ma dipende da quanti GPU hai fornito. Hai una delle seguenti opzioni. Dalla schermata dell'ordine di provisioning, hai una delle seguenti opzioni.
- Se viene fornita una GPU, puoi aggiungerne un'altra oppure
- Se vengono fornite due GPU, puoi tornare ad una
