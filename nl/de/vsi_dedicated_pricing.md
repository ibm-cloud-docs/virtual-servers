---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-22"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Preisstruktur für dedizierte Hosts
{: #dedicated-virtual-server-pricing}

Die Preise für dedizierte Hosts können auf Stundenbasis oder auf Monatsbasis abgerechnet werden.
{:shortdesc}

Die Preisstruktur für dedizierte Hosts schließt die Komponenten vCPU, Arbeitsspeicher, lokalen Speicher und Uplink-Port-Geschwindigkeit ein, da Instanzen auf dedizierten Hosts bereitgestellt werden. Weitere Informationen zur Preisstruktur finden Sie im Abschnitt zur [Berechnungsfunktion für die Bereitstellung virtueller Server ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

Für dedizierte Hosts sind zusätzlich lokale Speicherplatten auf der ersten, zweiten, dritten, vierten und fünften Platte verfügbar. Auf jeder sekundären Platte steht außerdem eine zusätzliche Kapazität von bis zu 400 GB zur Verfügung.

Instanzen auf Stundenbasis können auf Hosts mit einer Abrechnung auf Monats- oder Stundenbasis bereitgestellt werden. Instanzen auf Monatsbasis können nur auf Hosts mit einer Abrechnung auf Monatsbasis bereitgestellt werden.

| Hostkonfiguration | vCPU	| RAM (GB) | Lokaler Speicher (TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1,2  	     |  56 	|   242    |        	1,2	          |
| 56x484x1,2         |  56  |   484    |          1,2           |
{: caption="Tabelle 1. Konfigurationen für dedizierte Hosts" caption-side="top"}

Die Preisstruktur kann je nach Region variieren.
{:note}

SAN (ans Netz angeschlossen), Premium-Betriebssysteme und Software-Add-ons werden stündlich oder monatlich nach Instanz abgerechnet (abhängig von der auf dem dedizierten Host bereitgestellten Instanz). Die Preisstruktur für diese Komponenten entspricht dem bestehenden Angebot für öffentliche Instanzen und dedizierte Instanzen. 

Beispiel: Eine dedizierte Instanz, die auf einem dedizierten Host mit der folgenden Konfiguration bereitgestellt wird, wird nicht nach Instanz abgerechnet. vCPU, Arbeitsspeicher, lokaler Speicher und Uplink-Port-Geschwindigkeiten sind in den Gebühren für den dedizierten Host enthalten. 

* 8 vCPU
* 16 GB Arbeitsspeicher (RAM)
* 100 GB auf lokaler SSD als primärer Platte
* 400 GB auf lokaler SSD als sekundärer Platte
* 400 GB auf lokaler SSD als dritter Platte
* 1 Gb/s für öffentliche und private Netz-Uplinks (dedizierter Host) 

