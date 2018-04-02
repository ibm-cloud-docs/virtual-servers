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
GPU-Versionen (Flavors) sind am besten geeignet für Hochleistungs-Workloads, die eine größere Rechendichte zur Reduzierung von Ressourcenmanagement und Kosten erfordern. GPUs sind ideal für intensive Grafik- und Datenanwendungen oder für das Entwickeln neuer Anwendungen, die einen schnellen Durchsatz erfordern.

Angetrieben durch NVIDIA Tesla P100-GPUs, bietet die {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1”-Familie sowohl Blockspeicher (ac1) als auch lokalen SSD-Speicher (acl1). Sie können aus den folgenden GPU-Versionen (Flavors) auswählen:  

<table>

<caption>Tabelle 1. GPU-Versionen (Flavors)</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">GPU-Versionen (Flavors)</th>
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
  <th><b>GPU-RAM (GB)</b></th>
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
  <th><b>vCPU-RAM (GB)</b></th>
  <td>60</td>
  <td>60</td>
  <td>120</td>
  <td>120</td>
</tr>

<tr>
  <th><b>Speichertyp</b></th>
  <td>Block (SAN)</td>
  <td>Lokales SSD</td>
  <td>Block (SAN)</td>
  <td>Lokales SSD</td>
</tr>

<tr>
  <th><b>Bootdatenträger (GB)</b></th>
  <td>25 und 100</td>
  <td>100</td>
  <td>25 und 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>Sekundärer Datenträger (GB)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**Hinweis:** GPU-Versionen (Flavors) sind im Rechenzentrum _DAL13_ verfügbar.

## Vorbereitungen
Überprüfen Sie die folgenden GPU-Voraussetzungen.

1. Virtuelle Server der GPU-Familie sind nur auf einem Betriebssystem verfügbar, das den HVM-Bootmodus (HVM = Hardware Virtual Machine) unterstützt. Die folgende Liste enthält Betriebssysteme, die den HVM-Bootmodus unterstützen.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. Entsprechende NVIDIA-Treiber und Software müssen installiert werden. Weitere Informationen zu Software und NVIDIA-Treibern finden Sie unter [GPU-Treiber und -Softwarepakete installieren](../vsi/vsi_gpu_nvidia_drivers.html).

**Hinweis:** Die Software, die Sie installieren, erfordert möglicherweise bestimmte Softwarevoraussetzungen und betriebssystemspezifische Konfigurationen.


