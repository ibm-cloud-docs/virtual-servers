---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedizierte virtuelle Server
Bei dem Angebot für einen dedizierten Host in der {{site.data.keyword.Bluemix}}-Infrastruktur handelt es sich um einen virtuellen und dedizierten Einzel-Tenant-Server. Er bietet Ihnen maximale Kontrolle über die Workload-Platzierung und flexible Optionen nach der Bereitstellung. Sie können wählen, in welchem vordefinierten {{site.data.keyword.cloud}}-Rechenzentrum Ihre virtuellen Server platziert werden und zuverlässig eine bestimmte Kapazität reservieren, indem Sie Ihre Hosts direkt Ihrem Konto zuordnen.
{:shortdesc}

Das Angebot umfasst die folgenden Funktionen: 

* Affinität und Anti-Affinität. Sie können Beziehungen vom Host zum virtuellen Server (Affinitätsregeln) und vom virtuellen Server zum Host (Anti-Affinitätsregeln) angeben, die beibehalten werden sollen. Durch diese Regeln können Sie sicherstellen, dass Ihre Workloads gemäß Ihren Workload-Anforderungen platziert werden.
* Verwaltung nach der Bereitstellung. Sie können virtuelle Server entsprechend Ihren Workload-Anforderungen zwischen dedizierten Hosts migrieren.
* Sichtbarkeit der Workloads. Sie können die Ressourcenauslastung (Kern, Arbeitsspeicher und lokaler Speicher) für jeden Host anzeigen. Dies ermöglicht Ihnen die maximale Kontrolle über Ihr Workload-Management.

Sie können zwischen zwei Bereitstellungsmodellen wählen: dedizierte Hosts und dedizierte Instanzen. Dedizierte Hosts bieten mehr Kontrolle bei der Platzierung von Workloads und dedizierte Instanzen ermöglichen die Einzel-Tenant-Isolierung. 

**Hinweis:** In dedizierten Instanzen fehlen manche der Steuerfunktionen, die auf dedizierten Hosts zur Verfügung stehen. Weitere Details finden Sie in der folgenden Tabelle. 
<table>
<CAPTION>Tabelle 1. Steuerfunktionen</CAPTION>
<THEAD>
<TR>
<th>Funktion im dedizierten virtuellen Server</th>
<th>Dedizierte Hostinstanzen</th>
<th>Dedizierte Instanzen</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>Einzel-Tenant-Isolierung</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td>Platzierung für virtuelle Server steuern</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Sichtbarkeit der Ressourcen</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Abrechnung der Instanzen</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td>Abrechnung der Hosts<sup>(1)</sup></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Steuerungsmöglichkeiten nach der Bereitstellung</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Kapazitäten reservieren</td>
<td>X</td>
<td></td>
</tr>
</TBODY>
</table>


<sup>(1)</sup> Die Abrechnung für Hosts beinhaltet Kern, Arbeitsspeicher, lokale SSD und Netzgeschwindigkeit. Premium-Betriebssystem, SAN-Speicher (SAN = Storage Area Network) und Software-Add-ons werden pro Instanz gemäß der vorhandenen Preisstruktur und Lizenzierung auf Stunden- oder Monatsbasis abgerechnet.

Beachten Sie Folgendes beim Bestellen dedizierter Hosts und dedizierter Hostinstanzen:

* Ihren Host-Standort. Die folgenden {{site.data.keyword.cloud_notm}}-Rechenzentren stehen zur Auswahl:
      
| Rechenzentren          ||
| ------------ | ------- | 
|AMS01         |  MON01  |
|AMS03         |  OSL01  |
|CHE01         |  PAR01  |
|DAL05         |  SAO01  |
|DAL06         |  SEO01  |
|DAL09         |  SJC01  |
|DAL10         |  SJC03  |
|DAL12         |  SJC04  |
|DAL13         |  SNG01  | 
|FRA02         |  SYD01  |
|HKG02         |  SYD04  |
|HOU02         |  TOK02  |
|LON02         |  TOR01  |
|LON04         |  WDC01  |
|MEL01         |  WDC04  |
|MEX01         |  WDC06  |
|MIL01         |  WDC07  |
{: caption="Tabelle 2. Unterstützte Rechenzentren" caption-side="top"}

* Die Größe Ihrer Hosts wird durch die Workloads bestimmt, die darauf ausgeführt werden sollen. Die Standardeinstellung sind 56 Kerne X 242 GB RAM X 1,2 TB. 
* Sie können jeweils nur zwei Hosts auf einmal bestellen. Wenn Sie beispielsweise sechs Hosts benötigen, müssen Sie drei separate Bestellungen aufgeben.
* Für jeden Host ist ein eindeutiger Name erforderlich, und Sie können Ihren POD automatisch zuordnen.

## Nächste Schritte

Nachdem Sie Ihre Bereitstellungsoptionen geprüft und festgelegt haben, können Sie Ihren virtuellen Server bereitstellen lassen. Informationen zur Vorgehensweise finden Sie in [Dedizierte Hosts und Instanzen bereitstellen](../vsi/vsi_provision_dedicated.html).



  
