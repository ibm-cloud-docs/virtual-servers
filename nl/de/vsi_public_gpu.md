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
GPU-Versionen (Flavors) sind am besten geeignet für Hochleistungs-Workloads, die eine größere Rechendichte zur Reduzierung von Ressourcenmanagement und Kosten erfordern. Die GPU-Versionen (Flavors) sind ideal für intensive Grafik- und Datenanwendungen oder für das Entwickeln neuer Anwendungen, die einen schnellen Durchsatz erfordern.

Angetrieben durch NVDIA Tesla P100-GPUs bietet die {{site.data.keyword.cloud_notm}} Accelerated Compute-Version 'ac1' sowohl Blockspeicher als auch lokalen SSD-Speicher. Sie können aus den folgenden GPU-Versionen (Flavors) auswählen:  

  <table>
<CAPTION>Tabelle 1. GPU-Versionen (Flavors)</CAPTION>
<THEAD>
<TR>
<th>Version</th>
<th>GPU</th>
<th>GPU-RAM (GB)</th>
<th>vCPU</th>
<th>vCPU-RAM (GB)</th>
<th>Speichertyp</th>
<th>Bootdatenträger (GB)</th>
<th>Sekundärer Datenträger (GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Block (SAN)</td>
<td>25 und 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>1 P100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>Lokales SSD</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Block (SAN)</td>
<td>25 und 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>2 P100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>Lokales SSD</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**Hinweis:** GPU-Versionen (Flavors) stehen in den Rechenzentren _DAL13_, _LON06_ und _WDC07_ zur Verfügung.

## Vorbereitungen
Überprüfen Sie die folgenden GPU-Voraussetzungen.

1. Virtuelle Server mit GPU-Versionen sind nur auf einem Betriebssystem verfügbar, das den HVM-Bootmodus (HVM = Hardware Virtual Machine) unterstützt. Die folgende Liste enthält Betriebssysteme, die den HVM-Bootmodus unterstützen.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. Entsprechende NVIDIA-Treiber und Software müssen installiert werden. Weitere Informationen zu Software und NVIDIA-Treibern finden Sie unter [GPU-Treiber und -Softwarepakete installieren](../vsi/vsi_gpu_nvidia_drivers.html).  
**Hinweis:** Die Software, die Sie installieren, erfordert möglicherweise bestimmte Softwarevoraussetzungen und betriebssystemspezifische Konfigurationen.

# GPUs hinzufügen oder entfernen
Sie können die Anzahl der GPUs auf Ihrem virtuellen Server nach der Erstbestellung ändern. Dies hängt jedoch von der Zahl der von Ihnen insgesamt bereitgestellten GPUs ab. Sie können eine der folgenden Optionen auswählen. In der Anzeige für die Bereitstellungsbestellung können Sie eine der folgenden Optionen auswählen.
- Wenn eine GPU bereitgestellt ist, können Sie eine weitere GPU hinzufügen, oder:
- Wenn zwei GPUs bereitgestellt sind, können Sie auf eine einzige GPU zurücksetzen.
