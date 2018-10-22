---



copyright:
  years: 2017
lastupdated: "2017-11-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Archiviazione locale bilanciata
Le caratteristiche dell'archiviazione locale bilanciata sono pensate principalmente per i cluster del database grandi che richiedono prestazioni I/O di bassa o lata latenza. Questa offerta ha prestazioni elevate poiché le risorse non possono sottoscrivere più della disponibilità effettiva. Le prestazioni di rete vanno da standard a premium.

L'offerta è disponibile in varie caratteristiche e data center, con le seguenti opzioni di archiviazione locale:

* [HDD locale](vsi_public_balanced_local.html#HDD)
* [SSD locale](vsi_public_balanced_local.html#SSD)

## HDD locale {: #HDD}
 
<table>
<CAPTION>Tabella 1. Caratteristiche dell'archiviazione locale bilanciata con HDD locale</CAPTION>
<THEAD>
<TR>
<th>Caratteristica</th>
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

**Note di archiviazione:**
* <sup>(*)</sup>Le caratteristiche locali bilanciate vengono fornite automaticamente con un disco di avvio di memoria locale di 100 GB. Puoi quindi selezionare un secondo disco (opzioni mostrate nella tabella precedente). Tutti i dischi locali aggiuntivi sono facoltativi. Se hai bisogno di 500 GB, sono necessari due dischi aggiuntivi (ad esempio, 8 core richiedono 2 x 250 GB di memoria locale).
*	La memoria locale massima è limitata dai core. 
*	L'archiviazione locale bilanciata è globalmente disponibile; tuttavia, il tipo di archiviazione (SSD locale o HDD locale) dipende dall'ubicazione del data center. 
*	Non puoi scollegare i dischi primario o secondario.

I seguenti data center supportano i server virtuali di archiviazione locale bilanciata con HDD locale:

|Data center (HDD locale) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   | 
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="Tabella 1. Data center supportati (HDD locale)" caption-side="top"}

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta.  

## SSD locale {: #SSD}
<table>
<CAPTION>Tabella 1. Caratteristiche dell'archiviazione locale bilanciata con SSD locale</CAPTION>
<THEAD>
<TR>
<th>Caratteristica</th>
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

**Note di archiviazione:**
* <sup>(*)</sup>Le caratteristiche locali bilanciate vengono fornite automaticamente con un disco di avvio di memoria locale di 100 GB. Puoi quindi selezionare un secondo disco (opzioni mostrate nella tabella precedente). Tutti i dischi locali aggiuntivi sono facoltativi. Se hai bisogno di 500 GB, sono necessari due dischi aggiuntivi (ad esempio, 8 core richiedono 2 x 250 GB di memoria locale).
*	La memoria locale massima è limitata dai core. 
*	L'archiviazione locale bilanciata è globalmente disponibile; tuttavia, il tipo di archiviazione (SSD locale o HDD locale) dipende dall'ubicazione del data center. 
*	Non puoi scollegare i dischi primario o secondario.

I seguenti data center supportano i server virtuali di archiviazione locale bilanciata con SSD locale:

|Data center (SSD locale) |        |         |
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
{: caption="Tabella 2. Data center supportati (SSD locale)" caption-side="top"}

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta.  
