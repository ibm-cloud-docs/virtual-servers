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

# Profile
{: #about-virtual-server-profiles}

Bei der Bereitstellung von virtuellen {{site.data.keyword.cloud}}-Serverinstanzen können Sie zwischen verschiedenen unterstützten Profilfamilien wählen. Ein Profil gibt eine Kombination von vCPU und RAM an, die rasch instanziiert werden kann, um eine virtuelle Serverinstanz zu starten. In der {{site.data.keyword.cloud_notm}}-Konsole können Sie zwischen gängigen Profilkonfigurationen wählen oder eine Auswahl in einer Liste mit Profilen treffen, die am besten zur Erfüllung Ihrer Anforderungen geeignet sind.
{:shortdesc}

Die folgenden Familien von virtuellen Serverinstanzen stehen zur Verfügung.

Abhängig vom verwendeten Instanztyp stehen bestimmte Familien möglicherweise nicht zur Verfügung.
{:note}

| Familien  | Beschreibung                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
| [Ausgeglichen](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) | Besonders geeignet für gemeinsame Cloud-Workloads, für die eine Balance zwischen Leistung und Skalierbarkeit erforderlich ist. NAS (Network-attached Storage) wird verwendet. |
| [Ausgeglichener lokaler Speicher](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | Am besten geeignet für umfangreiche Datenbankworkloads mit hohen Anforderungen in Bezug auf die E/A-Leistung und sehr geringen Latenzzeiten. |
| [Compute](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) | Besonders geeignet für mittlere bis große Workloads im Webdatenverkehr. |
| [Speicher](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  | Besonders geeignet für Speichercache- und Echtzeitanalyse-Workloads. |
| [GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  | Besonders geeignet für Workloads, die eine hohe Leistung erfordern. |
{: caption="Tabelle 1. Optionen für Produktfamilie öffentlicher virtueller Server" caption-side="top"}

Einige dieser Produktfamilien sind auch für IBM Cloud Virtual Servers for VPC verfügbar. Weitere Informationen finden Sie in [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Ausgeglichen
{: #balanced}

Die ausgeglichenen Profile (mit NAS) sind ideal für allgemeine Cloud-Workloads geeignet, die einen Ausgleich der Leistung und Möglichkeiten zur Skalierung erfordern. Die Netzleistung liegt zwischen dem Standard- und dem Premiumbereich.

Für dieses Angebot stehen die folgenden Profile zur Verfügung:

| Profil   | vCPU    | RAM     | Speichertyp |
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
{: caption="Tabelle 2. Ausgeglichene Profile mit NAS" caption-side="top"}

### Hinweise zum Speicher

* Primärer SAN-Bootdatenträger (25 oder 100 GB) mit zusätzlich verfügbaren Datenträgern mit bis zu jeweils 2 TB (insgesamt fünf Datenträger zulässig).
* Die Preise für öffentliche virtuelle Server mit SAN-Speicher beinhalten virtuelle CPU, Hauptspeicher und einen primären Bootdatenträger in Mindestgröße. Die Preise für zusätzliche Datenträger sind von der ausgewählten Größe und Anzahl der Datenträger abhängig.  

Die ausgeglichenen Profile mit NAS sind in allen Rechenzentren verfügbar.

Alle unterstützten Betriebssysteme (z. B. RHEL, CentOS, Windows, Ubuntu und andere), Datenbanken und Software-Add-ons sind auch für dieses Angebot verfügbar. 

## Ausgeglichener lokaler Speicher
{: #balanced-local-storage}

Die Profile mit ausgeglichenem lokalem Speicher sind in erster Linie für umfangreiche Datenbankworkloads mit hohen Anforderungen in Bezug auf die E/A-Leistung und sehr geringen Latenzzeiten geeignet. Die Netzleistung liegt zwischen dem Standard- und dem Premiumbereich.

Das Angebot ist in verschiedenen Profilen und Rechenzentren mit den folgenden Optionen für lokalen Speicher verfügbar:

* [Lokales HDD](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [Lokales SSD](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### Lokales HDD
{: #HDD}
 
<table>
<CAPTION>Tabelle 3. Profile mit ausgeglichenem lokalem Speicher und Verwendung von lokalem HDD</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
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

#### Hinweise zum Speicher
* <sup>(*)</sup>Ausgeglichene lokale Profile beinhalten automatisch einen Bootdatenträger mit 100 GB für die lokale Speicherung. Anschließend können Sie einen zweiten Datenträger auswählen (Optionen finden Sie in Tabelle 3). Alle weiteren lokalen Datenträger sind optional. Wenn Sie mehr als 500 GB benötigen, sind zwei zusätzliche Datenträger erforderlich (Beispiel: für 8 Cores sind 2 x 250 GB lokaler Speicher erforderlich).
*	Der maximale lokale Speicher wird durch die Cores begrenzt. 
*	Ausgeglichener lokaler Speicher ist global verfügbar. Der Typ des Speichers (lokales SSD oder lokales HDD) ist jedoch vom Standort des Rechenzentrums abhängig. 
*	Primäre und sekundäre Datenträger können nicht abgehängt werden.

Die folgenden Rechenzentren unterstützen virtuelle Server mit ausgeglichenem lokalem Speicher mit lokalem HDD:

| Verfügbare Rechenzentren - Lokales HDD |       |
| ---------------------- | ----- |
| Dallas (DAL01)         | Dallas (DAL05)   |
| Dallas (DAL06)         | Houston (HOU02)  |
| Seattle (SEA01)        | San Jose (SJC01) |
| Washington, DC (WDC01) |                  |
{: class="simple-tab-table"}
{: caption="Tabelle 4. Verfügbare Rechenzentren (lokales HDD) - Nord- und Südamerika" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| Verfügbare Rechenzentren - Lokales HDD |
| ---------------------- |
| Amsterdam (AMS01)      |
{: class="simple-tab-table"}
{: caption="Tabelle 5. Verfügbare Rechenzentren (lokales HDD) - Europa" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| Verfügbare Rechenzentren - Lokales HDD |
| ---------------------- |
| Hong Kong (HKG02)      | 
| Singapore (SNG01)      |
{: class="simple-tab-table"}
{: caption="Tabelle 6. Verfügbare Rechenzentren (lokales HDD) - Asien/Pazifik" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

Alle unterstützten Betriebssysteme (z. B. RHEL, CentOS, Windows, Ubuntu und andere), Datenbanken und Software-Add-ons sind auch für dieses Angebot verfügbar.  

### Lokales SSD 
{: #SSD}

<table>
<CAPTION>Tabelle 7. Profile mit ausgeglichenem lokalem Speicher und Verwendung von lokalem SSD</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
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

#### Hinweise zum Speicher
* <sup>(*)</sup>Ausgeglichene lokale Profile beinhalten automatisch einen Bootdatenträger mit 100 GB für die lokale Speicherung. Anschließend können Sie einen zweiten Datenträger auswählen (Optionen finden Sie in der Tabelle oben). Alle weiteren lokalen Datenträger sind optional. Wenn Sie mehr als 500 GB benötigen, sind zwei zusätzliche Datenträger erforderlich (Beispiel: für 8 Cores sind 2 x 250 GB lokaler Speicher erforderlich).
*	Der maximale lokale Speicher wird durch die Cores begrenzt. 
*	Ausgeglichener lokaler Speicher ist global verfügbar. Der Typ des Speichers (lokales SSD oder lokales HDD) ist jedoch vom Standort des Rechenzentrums abhängig. 
*	Primäre und sekundäre Datenträger können nicht abgehängt werden.

Die folgenden Rechenzentren unterstützen virtuelle Server mit ausgeglichenem lokalem Speicher mit lokalem SSD:

| Verfügbare Rechenzentren - Lokales SDD |        |
| ---------------------------------- | ------ |
| Dallas (DAL09)                     | Dallas (DAL10)         |
| Dallas (DAL12)                     | Dallas (DAL13)         |
| Queretaro (MEX01)                  | Montreal (MON01)       |
| Sao Paulo (SAO01)                  | San Jose (SJC03)       |
| San Jose (SJC04)                   | Toronto (TOR01)        |
| Washington, DC (WDC04)             | Washington, DC (WDC06) |
| Washington, DC (WDC07)             |                        |
{: class="simple-tab-table"}
{: caption="Tabelle 8. Verfügbare Rechenzentren (lokales SDD) - Nord- und Südamerika" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| Verfügbare Rechenzentren - Lokales SDD |       |
| ---------------------------------- | ----- |
| Amsterdam (AMS03)                  | Frankfurt (FRA02) |
| London (LON02)                     | London (LON04)    |
| London (LON06)                     | Mailand (MIL01)     |
| Oslo (OSL01)                       | Paris (PAR01)     |
{: class="simple-tab-table"}
{: caption="Tabelle 9. Verfügbare Rechenzentren (lokales SDD) - Europa" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| Verfügbare Rechenzentren - Lokales SDD |       |
| ---------------------------------- | ----- |
| Chennai (CHE01)                    | Melbourne (MEL01) |
| Seoul (SEO01)                      | Sydney (SYD01)    |
| Sydney (SYD04)                     | Tokio (TOK02)     |
{: class="simple-tab-table"}
{: caption="Tabelle 10. Verfügbare Rechenzentren (lokales SDD) - Asien/Pazifik" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

Alle unterstützten Betriebssysteme (z. B. RHEL, CentOS, Windows, Ubuntu und andere), Datenbanken und Software-Add-ons sind auch für dieses Angebot verfügbar.

## Berechnung (Compute)
{: #compute}

Compute-Profile sind besonders geeignet für Workloads mit intensiver CPU-Nutzung (z. B. Workloads mit umfangreichem Webdatenverkehr, Stapelverarbeitung in der Produktionsumgebung oder Front-End-Web-Server).

Für dieses Angebot stehen die folgenden Profile zur Verfügung:

| Profil      | vCPU     | RAM       | Speichertyp |
| ------------ | -------- | --------- | ------------ |
| C1.1x1       | 1        | 1 GB      | SAN          |
| C1.2x2       | 2        | 2 GB      | SAN          |
| C1.4x4       | 4        | 4 GB      | SAN          |
| C1.8x8       | 8        | 8 GB      | SAN          |
| C1.16x16     | 16       | 16 GB     | SAN          |
| C1.32x32     | 32       | 32 GB     | SAN          |
{: caption="Tabelle 11. Compute-Profile" caption-side="top"}

### Hinweise zum Speicher
* Primärer SAN-Bootdatenträger (25 oder 100 GB) mit zusätzlich verfügbaren Datenträgern mit bis zu jeweils 2 TB (insgesamt fünf Datenträger zulässig).
* Die Preise für öffentliche virtuelle Server mit SAN-Speicher beinhalten virtuelle CPU, Hauptspeicher und einen primären Bootdatenträger in Mindestgröße. Die Preise für zusätzliche Datenträger sind von der ausgewählten Größe und Anzahl der Datenträger abhängig.  

Compute-Profile sind in allen Rechenzentren verfügbar.

Alle unterstützten Betriebssysteme (z. B. RHEL, CentOS, Windows, Ubuntu und andere), Datenbanken und Software-Add-ons sind auch für dieses Angebot verfügbar.

## Speicher
{: #memory}

Speicherbetonte Profile sind besonders geeignet für speicherintensive Workloads (z. B. umfangreiche Caching-Workloads, rechenintensive Datenbankanwendungen oder speicherinterne Analyse-Workloads).

Für dieses Angebot stehen die folgenden Profile zur Verfügung:

| Profil      | vCPU     | RAM       | Speichertyp |
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
{: caption="Tabelle 12. Speicherbetonte Profile" caption-side="top"}

### Hinweise zum Speicher
* Primärer SAN-Bootdatenträger (25 oder 100 GB) mit verfügbaren zusätzlichen Datenträgern mit bis zu jeweils 2 TB (5 Datenträger insgesamt zulässig).
* Die Preise für öffentliche virtuelle Server mit SAN-Speicher beinhalten virtuelle CPU, Hauptspeicher und einen primären Bootdatenträger in Mindestgröße. Die Preise für zusätzliche Datenträger sind von der ausgewählten Größe und Menge der Datenträger abhängig.  

Speicherbetonte Profile sind in allen Rechenzentren verfügbar.

Alle unterstützten Betriebssysteme (z. B. RHEL, CentOS, Windows, Ubuntu und andere), Datenbanken und Software-Add-ons sind auch für dieses Angebot verfügbar.

## GPU
{: #gpu}

GPU-Profile sind am besten geeignet für Hochleistungs-Workloads, die eine größere Rechendichte erfordern, um den Aufwand für das Ressourcenmanagement zu verringern und Kosten einzusparen. Die GPU-Profile sind ideal für auf künstlicher Intelligenz basierende Prozesse, intensive Grafik- und Datenanwendungen oder für das Entwickeln neuer Anwendungen, die einen schnellen Durchsatz erfordern.

Unterstützt durch NVDIA Tesla-GPUs bieten die {{site.data.keyword.cloud_notm}} Accelerated Compute-Profile 'ac1' und 'ac2' Blockspeicher und lokalen SSD-Speicher. Sie können aus den folgenden GPU-Profilen auswählen:  

<table>
<CAPTION>Tabelle 13. P100-GPU-Profile</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
<th>GPU</th>
<th>GPU-RAM (GB)</th>
<th>vCPU</th>
<th>vCPU-RAM (GB)</th>
<th>Speichertyp</th>
<th>Bootdatenträger (GB)</th>
<th>Sekundäre Datenträger (2 und 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Block (SAN)</td>
<td>25</td>
<td>0</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Lokale SSD oder SAN</td>
<td>100</td>
<td>0 (SAN)<br>300 (Lokal)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Block (SAN)</td>
<td>25</td>
<td>0</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Lokale SSD oder SAN</td>
<td>100</td>
<td>0 (SAN)<br>600 (Lokal)</td></tr>

</TBODY>
</table>

P100-GPU-Profile stehen in den Rechenzentren _DAL13_, _LON06_ und _WDC07_ zur Verfügung.
{: note}

<table>
<CAPTION>Tabelle 14. V100-GPU-Profile</CAPTION>
<THEAD>
<TR>
<th>Profil</th>
<th>GPU</th>
<th>GPU-RAM (GB)</th>
<th>vCPU</th>
<th>vCPU-RAM (GB)</th>
<th>Speichertyp</th>
<th>Bootdatenträger (GB)</th>
<th>Sekundäre Datenträger (2 und 3) (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Block (SAN)</td>
<td>25</td>
<td>0</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Lokale SSD oder SAN</td>
<td>100</td>
<td>0 (SAN)<br>300 (Lokal)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Block (SAN)</td>
<td>25</td>
<td>0</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Lokale SSD oder SAN</td>
<td>100</td>
<td>0 (SAN)<br>600 (Lokal)</td></tr>

</TBODY>
</table>

V100-GPU-Profile stehen in den Rechenzentren _DAL10_, _DAL12_ sowie _LON04_ und _WDC07_ zur Verfügung.
{: note}

### GPU-Voraussetzungen
Überprüfen Sie die folgenden GPU-Voraussetzungen.

1. Virtuelle Server mit GPU-Profilen sind nur auf einem Betriebssystem verfügbar, das den HVM-Bootmodus (HVM = Hardware Virtual Machine) unterstützt. Die folgende Liste enthält Betriebssysteme, die den HVM-Bootmodus unterstützen.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Entsprechende NVIDIA-Treiber und Software müssen installiert werden. Weitere Informationen zu Software und NVIDIA-Treibern finden Sie unter [GPU-Treiber und -Softwarepakete installieren](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages).  

Die Software, die Sie installieren, erfordert möglicherweise bestimmte Softwarevoraussetzungen und betriebssystemspezifische Konfigurationen.
{: note}

### GPUs hinzufügen oder entfernen 
Sie können die Anzahl der GPUs auf Ihrem virtuellen Server nach der Erstbestellung ändern. Dies hängt jedoch von der Zahl der von Ihnen insgesamt bereitgestellten GPUs ab. Sie können eine der folgenden Optionen auswählen.

- Wenn eine GPU bereitgestellt ist, können Sie eine weitere GPU hinzufügen, oder:
- Wenn zwei GPUs bereitgestellt sind, können Sie auf eine einzige GPU zurücksetzen.

