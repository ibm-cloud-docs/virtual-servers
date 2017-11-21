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

# Ausgeglichener lokaler Speicher
Die Versionen (Flavors) mit ausgeglichenem lokalem Speicher sind in erster Linie für große Datenbankcluster geeignet, für die eine E/A-Leistung mit hohen oder niedrigen Latenzzeiten erforderlich ist. Dieses Angebot bietet eine höhere Leistung, da die Ressourcen nicht übermäßig beansprucht werden. Die Netzleistung liegt zwischen dem Standard- und dem Premiumbereich.

Das Angebot ist in verschiedenen Versionen und Rechenzentren mit den folgenden Optionen für lokalen Speicher verfügbar:

* [Lokales HDD](vsi_public_balanced_local.html#HDD)
* [Lokales SSD](vsi_public_balanced_local.html#SSD)

## Lokales HDD {: #HDD}
 
<table>
<CAPTION>Tabelle 1. Versionen (Flavors) mit ausgeglichenem lokalem Speicher und Verwendung von lokalem HDD</CAPTION>
<THEAD>
<TR>
<th>Version</th>
<th>vCPU</th>
<th>RAM</th>
<th>Sekundäre Platten<sup>(*)</sup></th>
<th>Speichertyp</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Lokales HDD</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Lokales HDD</td>
</tr>
</TBODY>
</table>

**Hinweise zum Speicher:**
* <sup>(*)</sup> Ausgeglichene lokale Versionen (Flavors) beinhalten automatisch einen Bootdatenträger mit 100 GB für die lokale Speicherung. Anschließend können Sie einen zweiten Datenträger auswählen (Optionen finden Sie in der Tabelle oben). Alle weiteren lokalen Datenträger sind optional. Wenn Sie mehr als 500 GB benötigen, sind zwei zusätzliche Datenträger erforderlich (Beispiel: für 8 Kerne sind 2 x 250 GB lokaler Speicher erforderlich).
*	Der maximale lokale Speicher wird durch die Kerne begrenzt. 
*	Ausgeglichener lokaler Speicher ist global verfügbar. Der Typ des Speichers (Lokales SSD oder Lokales HDD) ist jedoch vom Standort des Rechenzentrums abhängig. 
*	Primäre und sekundäre Datenträger können nicht abgehängt werden.

Die folgenden Rechenzentren unterstützen virtuelle Server mit ausgeglichenem lokalem HDD-Speicher:

|Rechenzentren (Lokales HDD) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   | 
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="Tabelle 1. Unterstützte Rechenzentren (Lokales HDD)" caption-side="top"}

Alle unterstützten Betriebssysteme (z. B. RHEL, CentOS, Windows, Ubuntu und andere), Datenbanken und Software-Add-ons sind auch für dieses Angebot verfügbar.  

## Lokales SSD {: #SSD}
<table>
<CAPTION>Tabelle 1. Versionen (Flavors) mit ausgeglichenem lokalem Speicher und Verwendung von lokalem SSD</CAPTION>
<THEAD>
<TR>
<th>Version</th>
<th>vCPU</th>
<th>RAM</th>
<th>Sekundäre Platten<sup>(*)</sup></th>
<th>Speichertyp</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2 GB</td>
<td>25, 100 GB</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4 GB</td>
<td>25, 100 GB</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4 GB</td>
<td>100, 200 GB</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8 GB</td>
<td>100, 200 GB</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8 GB</td>
<td>150, 300 GB</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16 GB</td>
<td>150, 300 GB</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32 GB</td>
<td>250 GB, (2 x 250 GB)</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64 GB</td>
<td>300 GB, (2 x 300 GB)</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Lokales SSD</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128 GB</td>
<td>400 GB, (2 x 400 GB)</td>
<td>Lokales SSD</td>
</tr>
</TBODY>
</table>

**Hinweise zum Speicher:**
* <sup>(*)</sup> Ausgeglichene lokale Flavors (Versionen) beinhalten automatisch einen Bootdatenträger mit 100 GB für die lokale Speicherung. Anschließend können Sie einen zweiten Datenträger auswählen (Optionen finden Sie in der Tabelle oben). Alle weiteren lokalen Datenträger sind optional. Wenn Sie mehr als 500 GB benötigen, sind zwei zusätzliche Datenträger erforderlich (Beispiel: für 8 Kerne sind 2 x 250 GB lokaler Speicher erforderlich).
*	Der maximale lokale Speicher wird durch die Kerne begrenzt. 
*	Ausgeglichener lokaler Speicher ist global verfügbar. Der Typ des Speichers (Lokales SSD oder Lokales HDD) ist jedoch von der Position des Rechenzentrums abhängig. 
*	Primäre und sekundäre Datenträger können nicht abgehängt werden.

Die folgenden Rechenzentren unterstützen virtuelle Server mit ausgeglichenem lokalem SSD-Speicher:

|Rechenzentren (Lokales SSD) |        |         |
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
{: caption="Tabelle 2. Unterstützte Rechenzentren (Lokales SSD)" caption-side="top"}

Alle unterstützten Betriebssysteme (z. B. RHEL, CentOS, Windows, Ubuntu und andere), Datenbanken und Software-Add-ons sind auch für dieses Angebot verfügbar.  
