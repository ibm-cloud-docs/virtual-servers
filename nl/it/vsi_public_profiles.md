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

# Profili
{: #about-virtual-server-profiles}

Quando esegui il provisioning delle istanze del server virtuale {{site.data.keyword.cloud}}, puoi scegliere tra le famiglie di profili supportate. Un profilo è una combinazione di vCPU e RAM che può essere istanziato velocemente per avviare un'istanza del server virtuale. Nella console {{site.data.keyword.cloud_notm}}, puoi scegliere tra le configurazioni di profilo popolare oppure da un elenco di profili che meglio si adattano alle tue esigenze.
{:shortdesc}

Sono disponibili le seguenti famiglie di istanze del server virtuale.

A seconda del tuo tipo di istanza, alcune famiglie potrebbero non essere disponibili.
{:note}

| Famiglie  | Descrizione                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Bilanciato](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Migliore per i carichi di lavoro cloud comuni che richiedono un bilanciamento di prestazioni e scalabilità. Utilizza l'archiviazione assegnata di rete. |
| [Archiviazione locale bilanciata](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | Migliore per grandi carichi di lavoro di database che richiedono prestazioni I/O elevate e latenza molto bassa. |
| [Calcolo](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Migliore per i carichi di lavoro con traffico web da moderato a elevato. |
| [Memoria](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Migliore per la memorizzazione nella cache e i carichi di lavoro di analisi in tempo reale. |
| [GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  | Migliore per i carichi di lavoro ad elevate prestazioni. |
{: caption="Tabella 1. Selezioni di famiglie del server virtuale pubblico" caption-side="top"}

Alcune di queste famiglie sono anche disponibili per IBM Cloud Virtual Servers for VPC. Per ulteriori informazioni, consulta [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Bilanciato
{: #balanced}

I profili bilanciati (con l'archiviazione collegata alla rete) sono ideali per i carichi di lavoro cloud comuni che richiedono un bilanciamento di prestazioni e scalabilità. Le prestazioni di rete vanno da standard a premium.

L'offerta è disponibile nei seguenti profili:

| Profilo   | vCPU    | RAM     | Tipo di archiviazione |
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
{: caption="Tabella 2. Profili bilanciati con l'archiviazione collegata alla rete" caption-side="top"}

### Note di archiviazione

* Disco di avvio primario SAN (25 o 100 GB) con dischi aggiuntivi disponibili, fino a 2 TB ciascuno (cinque dischi totali consentiti).
* I prezzi per i server virtuali pubblici che utilizzano l'archiviazione SAN includono CPU virtuale, memoria e disco di avvio primario minimo. I prezzi di ulteriori dischi dipendono dalla dimensione e dalla quantità che selezioni.  

I profili bilanciati (con l'archiviazione collegata alla rete) sono disponibili in tutti i data center.

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta. 

## Archiviazione locale bilanciata
{: #balanced-local-storage}

I profili dell'archiviazione locale bilanciata sono pensati principalmente per grandi carichi di lavoro di database che richiedono prestazioni I/O elevate e latenza molto bassa. Le prestazioni di rete vanno da standard a premium.

L'offerta è disponibile in vari profili e data center, con le seguenti opzioni di archiviazione locale:

* [HDD locale ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [SSD locale ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### HDD locale
{: #HDD}
 
<table>
<CAPTION>Tabella 3. Profili dell'archiviazione locale bilanciata con HDD locale</CAPTION>
<THEAD>
<TR>
<th>Profilo</th>
<th>vCPU</th>
<th>RAM</th>
<th>Dischi secondari<sup>(*)</sup></th>
<th>Tipo di archiviazione</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>HDD locale</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>HDD locale</td>
</tr>
</TBODY>
</table>

#### Note di archiviazione
* <sup>(*)</sup>I profili locali bilanciati vengono forniti automaticamente con un disco di avvio di memoria locale di 100 GB. Puoi quindi selezionare un secondo disco (opzioni mostrate nella tabella 3). Tutti i dischi locali aggiuntivi sono facoltativi. Se hai bisogno di 500 GB, sono necessari due dischi aggiuntivi (ad esempio, 8 core richiedono 2 x 250 GB di memoria locale).
*	La memoria locale massima è limitata dai core. 
*	L'archiviazione locale bilanciata è globalmente disponibile; tuttavia, il tipo di archiviazione (SSD locale o HDD locale) dipende dall'ubicazione del data center. 
*	Non puoi scollegare i dischi primario o secondario.

I seguenti data center supportano i server virtuali di archiviazione locale bilanciata con HDD locale:

| Data Center disponibili - HDD locale |       |
| ---------------------- | ----- |
| Dallas (DAL01)         | Dallas (DAL05)   |
| Dallas (DAL06)         | Houston (HOU02)  |
| Seattle (SEA01)        | San Jose (SJC01) |
| Washington, DC (WDC01) |                  |
{: class="simple-tab-table"}
{: caption="Tabella 4. Data center disponibili (HDD locale) - Americhe" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| Data Center disponibili - HDD locale |
| ---------------------- |
| Amsterdam (AMS01)      |
{: class="simple-tab-table"}
{: caption="Tabella 5. Data center disponibili (HDD locale) - Europa" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| Data Center disponibili - HDD locale |
| ---------------------- |
| Hong Kong (HKG02)      | 
| Singapore (SNG01)      |
{: class="simple-tab-table"}
{: caption="Tabella 6. Data center disponibili (HDD locale) - Asia e pacifico" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta.  

### SSD locale 
{: #SSD}

<table>
<CAPTION>Tabella 7. Profili dell'archiviazione locale bilanciata con SSD locale</CAPTION>
<THEAD>
<TR>
<th>Profilo</th>
<th>vCPU</th>
<th>RAM</th>
<th>Dischi secondari<sup>(*)</sup></th>
<th>Tipo di archiviazione</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>SSD locale</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>SSD locale</td>
</tr>
</TBODY>
</table>

#### Note di archiviazione
* <sup>(*)</sup>I profili locali bilanciati vengono forniti automaticamente con un disco di avvio di memoria locale di 100 GB. Puoi quindi selezionare un secondo disco (opzioni mostrate nella tabella precedente). Tutti i dischi locali aggiuntivi sono facoltativi. Se hai bisogno di 500 GB, sono necessari due dischi aggiuntivi (ad esempio, 8 core richiedono 2 x 250 GB di memoria locale).
*	La memoria locale massima è limitata dai core. 
*	L'archiviazione locale bilanciata è globalmente disponibile; tuttavia, il tipo di archiviazione (SSD locale o HDD locale) dipende dall'ubicazione del data center. 
*	Non puoi scollegare i dischi primario o secondario.

I seguenti data center supportano i server virtuali di archiviazione locale bilanciata con SSD locale:

| Data Center disponibili - SDD locale |        |
| ---------------------------------- | ------ |
| Dallas (DAL09)                     | Dallas (DAL10)         |
| Dallas (DAL12)                     | Dallas (DAL13)         |
| Queretaro (MEX01)                  | Montreal (MON01)       |
| Sao Paulo (SAO01)                  | San Jose (SJC03)       |
| San Jose (SJC04)                   | Toronto (TOR01)        |
| Washington, DC (WDC04)             | Washington, DC (WDC06) |
| Washington, DC (WDC07)             |                        |
{: class="simple-tab-table"}
{: caption="Tabella 8. Data center disponibili (SDD locale) - Americhe" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| Data Center disponibili - SDD locale |       |
| ---------------------------------- | ----- |
| Amsterdam (AMS03)                  | Francoforte (FRA02)|
| Londra (LON02)                     | Londra (LON04)    |
| Londra (LON06)                     | Milano (MIL01)     |
| Oslo (OSL01)                       | Parigi (PAR01)     |
{: class="simple-tab-table"}
{: caption="Tabella 9. Data center disponibili (SDD locale) - Europa" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| Data Center disponibili - SDD locale |       |
| ---------------------------------- | ----- |
| Chennai (CHE01)                    | Melbourne (MEL01) |
| Seoul (SEO01)                      | Sydney (SYD01)    |
| Sydney (SYD04)                     | Tokyo (TOK02)     |
{: class="simple-tab-table"}
{: caption="Tabella 10. Data center disponibili (SDD locale) - Asia e pacifico" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta.

## Calcolo
{: #compute}

I profili di calcolo sono migliori per i carichi di lavoro con richiesta di CPU intensiva, come i carichi di lavoro di traffico web elevato, l'elaborazione batch di produzione e i server web di frontend.

L'offerta è disponibile nei seguenti profili:

| Profilo      | vCPU     | RAM       | Tipo di archiviazione |
| ------------ | -------- | --------- | ------------ |
| C1.1x1       | 1        | 1 GB      | SAN          |
| C1.2x2       | 2        | 2 GB      | SAN          |
| C1.4x4       | 4        | 4 GB      | SAN          |
| C1.8x8       | 8        | 8 GB      | SAN          |
| C1.16x16     | 16       | 16 GB     | SAN          |
| C1.32x32     | 32       | 32 GB     | SAN          |
{: caption="Tabella 11. Profili di calcolo" caption-side="top"}

### Note di archiviazione
* Disco di avvio primario SAN (25 o 100 GB) con dischi aggiuntivi disponibili, fino a 2 TB ciascuno (cinque dischi totali consentiti).
* I prezzi per i server virtuali pubblici che utilizzano l'archiviazione SAN includono CPU virtuale, memoria e disco di avvio primario minimo. I prezzi di ulteriori dischi dipendono dalla dimensione e dalla quantità che selezioni.  

I profili di calcolo sono disponibili in tutti i data center.

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta.

## Memoria
{: #memory}

I profili di memoria sono migliori per i carichi di lavoro con uso intensivo di memoria, come i grandi carichi di lavoro con memorizzazione in cache, le applicazioni database intensive o i carichi di lavoro di analisi nella memoria.

L'offerta è disponibile nei seguenti profili:

| Profilo      | vCPU     | RAM       | Tipo di archiviazione |
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
{: caption="Tabella 12. Profili di memoria" caption-side="top"}

### Note di archiviazione
* Disco di avvio primario SAN (25 o 100 GB) con dischi aggiuntivi disponibili, fino a 2 TB ciascuno (5 dischi totali consentiti).
* I prezzi per i server virtuali pubblici che utilizzano l'archiviazione SAN includono CPU virtuale, memoria e disco di avvio primario minimo. I prezzi di ulteriori dischi dipendono dalla dimensione e dalla quantità che selezioni.  

I profili di memoria sono disponibili in tutti i data center.

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta.

## GPU
{: #gpu}

I profili GPU sono migliori per i carichi di lavoro dalle prestazioni elevate che richiedono più densità di calcolo per ridurre la gestione delle risorse e i costi. I profili GPU sono ideali per i processi di intelligenza artificiale, le applicazioni di dati e grafiche intense o per lo sviluppo di nuove applicazioni che richiedono prestazioni veloci.

Con tecnologia NVDIA Tesla GPUs, i profili {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” e "ac2" offrono entrambi l'archiviazione blocchi e SSD locale. I seguenti profili GPU sono disponibili per la tua scelta:  

<table>
<CAPTION>Tabella 13. Profili P100 GPU</CAPTION>
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

I profili P100 GPU sono disponibili nei data center _DAL13_, _LON06_ e _WDC07_.
{: note}

<table>
<CAPTION>Tabella 14. Profili V100 GPU</CAPTION>
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

I profili V100 GPU sono disponibili nei data center _DAL10_, _DAL12_, _LON04_ e _WDC07_.
{: note}

### Prerequisiti GPU
Controlla i seguenti prerequisiti GPU.

1. I server virtuali del profilo GPU sono disponibili solo su un sistema operativo che supporta la modalità di avvio HVM (Hardware Virtual Machine). Consulta il seguente elenco per i sistemi operativi che supportano la modalità di avvio HVM.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Devono essere installati il software e i driver NVIDIA appropriati. Per ulteriori informazioni sul software e sui driver NVIDIA, consulta [Installazione dei driver GPU dai pacchetti software](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages).  

Il software che istalli potrebbe avere del software prerequisito e delle configurazioni specifiche per sistema operativo.
{: note}

### Aggiunta o rimozione di GPU 
Puoi modificare il numero di GPU sul tuo server virtuale dopo l'ordine iniziale. Ma dipende da quanti GPU hai fornito. Hai una delle seguenti opzioni.

- Se viene fornita una GPU, puoi aggiungerne un'altra oppure
- Se vengono fornite due GPU, puoi tornare ad una

