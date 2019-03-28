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

I profili GPU sono migliori per i carichi di lavoro dalle prestazioni elevate che richiedono più densità di calcolo per ridurre la gestione delle risorse e i costi. I profili GPU sono ideali per i processi di intelligenza artificiale, le applicazioni di dati e grafiche intense o per lo sviluppo di nuove applicazioni che richiedono prestazioni veloci. 

Con tecnologia NVDIA Tesla GPUs, le caratteristiche {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” e "ac2" offrono entrambe l'archiviazione blocchi e SSD locale. I seguenti profili GPU sono disponibili per la tua scelta:  

  <table>
<CAPTION>Tabella 1. Profili P100 GPU</CAPTION>
<THEAD>
<TR>
<th>Profilo</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>Tipo di archiviazione</th>
<th>Disco di avvio (GB)</th>
<th>Dischi secondari (2 e 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Blocchi (SAN)</td>
<td>25</td>
<td>Nessuno</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD locale o SAN</td>
<td>100</td>
<td>Nessuno (SAN)<br>300 (Locale)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Blocchi (SAN)</td>
<td>25</td>
<td>Nessuno</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD locale o SAN</td>
<td>100</td>
<td>Nessuno (SAN)<br>600 (Locale)</td></tr>

</TBODY>
</table>

**Nota:** i profili P100 GPU sono disponibili nei data center _DAL13_, _LON06_ e _WDC07_.

<table>
<CAPTION>Tabella 2. Profili V100 GPU</CAPTION>
<THEAD>
<TR>
<th>Profilo</th>
<th>GPU</th>
<th>GPU RAM (GB)</th>
<th>vCPU</th>
<th>vCPU RAM (GB)</th>
<th>Tipo di archiviazione</th>
<th>Disco di avvio (GB)</th>
<th>Dischi secondari (2 e 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Blocchi (SAN)</td>
<td>25</td>
<td>Nessuno</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>SSD locale o SAN</td>
<td>100</td>
<td>Nessuno (SAN)<br>300 (Locale)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Blocchi (SAN)</td>
<td>25</td>
<td>Nessuno</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>SSD locale o SAN</td>
<td>100</td>
<td>Nessuno (SAN)<br>600 (Locale)</td></tr>

</TBODY>
</table>

**Nota:** i profili V100 GPU sono disponibili nei data center _DAL10_, _DAL12_, _LON04_ e _WDC07_.


## Informazioni preliminari
Controlla i seguenti prerequisiti GPU.

1. I server virtuali del profilo GPU sono disponibili solo su un sistema operativo che supporta la modalità di avvio HVM (Hardware Virtual Machine). Consulta il seguente elenco per i sistemi operativi che supportano la modalità di avvio HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Devono essere installati il software e i driver NVIDIA appropriati. Per ulteriori informazioni sul software e sui driver NVIDIA, consulta [Installazione dei driver GPU dai pacchetti software](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages).  
**Nota:** il software che istalli potrebbe avere del software prerequisito e delle configurazioni specifiche per sistema operativo.

## Aggiungi o rimuovi GPU
Puoi modificare il numero di GPU sul tuo server virtuale dopo l'ordine iniziale. Ma dipende da quanti GPU hai fornito. Hai una delle seguenti opzioni.

- Se viene fornita una GPU, puoi aggiungerne un'altra oppure
- Se vengono fornite due GPU, puoi tornare ad una
