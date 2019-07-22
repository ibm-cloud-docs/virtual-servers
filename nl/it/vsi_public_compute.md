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

# Calcolo
{: #compute}

I profili di calcolo sono migliori per i carichi di lavoro con richiesta di CPU intensiva, come i carichi di lavoro di traffico web elevato, l'elaborazione batch di produzione e i server web di frontend.

L'offerta è disponibile nei seguenti profili:

<table>
<CAPTION>Tabella 1. Profili di calcolo</CAPTION>
<THEAD>
<TR>
<th>Profilo</th>
<th>vCPU</th>
<th>RAM</th>
<th>Tipo di archiviazione</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>C1.1x1</td>
<td>1</td>
<td>1 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.2x2</td>
<td>2</td>
<td>2 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.4x4</td>
<td>4</td>
<td>4 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.8x8</td>
<td>8</td>
<td>8 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.16x16</td>
<td>16</td>
<td>16 GB</td>
<td>SAN</td>
</tr>
<tr>
<td>C1.32x32</td>
<td>32</td>
<td>32 GB</td>
<td>SAN</td>
</tr>
</TBODY>
</table>

**Note di archiviazione:**
* Disco di avvio primario SAN (25 o 100 GB) con dischi aggiuntivi disponibili, fino a 2 TB ciascuno (5 dischi totali consentiti).
* I prezzi per i server virtuali pubblici che utilizzano l'archiviazione SAN includono CPU virtuale, memoria e disco di avvio primario minimo. I prezzi di ulteriori dischi dipendono dalla dimensione e dalla quantità che selezioni.  

I profili di calcolo sono disponibili in tutti i data center.

Tutti i sistemi operativi supportati (come RHEL, CentOS, Windows, Ubuntu e altri), i database supportati e i componenti aggiuntivi software sono inoltre disponibili con questa offerta.  
