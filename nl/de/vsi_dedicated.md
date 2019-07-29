---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:row-headers: .row-headers}
{:table: .aria-labeledby="caption"}


# Informationen zu dedizierten virtuellen Servern
{: #dedicated-virtual-servers}

Bei dem Angebot für einen dedizierten Host in der {{site.data.keyword.Bluemix}}-Infrastruktur handelt es sich um einen virtuellen und dedizierten Einzel-Tenant-Server. Er bietet Ihnen maximale Kontrolle über die Workload-Platzierung und flexible Optionen nach der Bereitstellung. Sie können wählen, in welchem vordefinierten {{site.data.keyword.cloud_notm}}-Rechenzentrum Ihre virtuellen Server platziert werden und zuverlässig eine bestimmte Kapazität reservieren, indem Sie Ihre Hosts direkt Ihrem Konto zuordnen.
{:shortdesc}

Das Angebot umfasst die folgenden Funktionen:

* Affinität und Anti-Affinität. Sie können Beziehungen vom Host zum virtuellen Server (Affinitätsregeln) und vom virtuellen Server zum Host (Anti-Affinitätsregeln) angeben, die beibehalten werden sollen. Durch diese Regeln können Sie sicherstellen, dass Ihre Workloads gemäß Ihren Workload-Anforderungen platziert werden.
* Verwaltung nach der Bereitstellung. Sie können virtuelle Server entsprechend Ihren Workload-Anforderungen zwischen dedizierten Hosts migrieren.
* Sichtbarkeit der Workloads. Sie können die Ressourcenauslastung (Core, Arbeitsspeicher und lokaler Speicher) für jeden Host anzeigen. Dies ermöglicht Ihnen die maximale Kontrolle über Ihr Workload-Management.

Sie können zwischen zwei Bereitstellungsmodellen wählen: dedizierte Hosts und dedizierte Instanzen. Dedizierte Hosts bieten mehr Kontrolle bei der Platzierung von Workloads und dedizierte Instanzen ermöglichen die Einzel-Tenant-Isolierung.

In dedizierten Instanzen fehlen manche der Steuerfunktionen, die auf dedizierten Hosts zur Verfügung stehen. Weitere Details finden Sie in der folgenden Tabelle.
{:note}

| Funktion im dedizierten virtuellen Server | Dedizierte Hostinstanzen | Dedizierte Instanzen |
| ------- | ------- | ------- |
| Einzel-Tenant-Isolierung | ![Häkchensymbol](../../icons/checkmark-icon.svg) | ![Häkchensymbol](../../icons/checkmark-icon.svg) |
| Platzierung für virtuelle Server steuern | ![Häkchensymbol](../../icons/checkmark-icon.svg) |   |
| Sichtbarkeit der Ressourcen | ![Häkchensymbol](../../icons/checkmark-icon.svg) |   |
| Abrechnung der Instanzen |   | ![Häkchensymbol](../../icons/checkmark-icon.svg) |
| Abrechnung der Hosts<sup>(1)</sup> | ![Häkchensymbol](../../icons/checkmark-icon.svg) |   |
| Steuerungsmöglichkeiten nach der Bereitstellung | ![Häkchensymbol](../../icons/checkmark-icon.svg) |   |
| Kapazitäten reservieren | ![Häkchensymbol](../../icons/checkmark-icon.svg) |   |
{: row-headers}
{: class="comparison-table}
{: caption="Tabelle 1. Steuerfunktionen" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the control feature. The column headers identify whether the offering offers the control feature. To understand whether the offering offers the control feature, navigate to the row in the table, and find the offering you are interested in.}

<sup>(1)</sup> Die Abrechnung für Hosts beinhaltet Core, Arbeitsspeicher, lokale SSD und Netzgeschwindigkeit. Premium-Betriebssystem, SAN-Speicher (SAN = Storage Area Network) und Software-Add-ons werden pro Instanz gemäß der vorhandenen Preisstruktur und Lizenzierung auf Stunden- oder Monatsbasis abgerechnet.

Beachten Sie Folgendes beim Bestellen dedizierter Hosts und dedizierter Hostinstanzen:

* Die Größe Ihrer Hosts wird durch die Workloads bestimmt, die darauf ausgeführt werden sollen. Die Standardeinstellung sind 56 Cores X 242 GB RAM X 1,2 TB, Sie können jedoch auch zusätzliche Konfigurationen auswählen.
* Sie können jeweils nur zwei Hosts auf einmal bestellen. Wenn Sie beispielsweise sechs Hosts benötigen, müssen Sie drei separate Bestellungen aufgeben.
* Für jeden Host ist ein eindeutiger Name erforderlich, und Sie können Ihren POD automatisch zuordnen.

## Nächste Schritte

Nachdem Sie Ihre Bereitstellungsoptionen geprüft und festgelegt haben, können Sie Ihren virtuellen Server bereitstellen lassen. Informationen zur Vorgehensweise finden Sie in [Dedizierte Hosts und Instanzen bereitstellen](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated).
