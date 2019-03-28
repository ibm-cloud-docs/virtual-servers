---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Preisstruktur für dedizierte virtuelle Server
{: #dedicated-virtual-server-pricing}

Die Preise für dedizierte Hosts können auf Stundenbasis oder auf Monatsbasis abgerechnet werden.
{:shortdesc}

Die Preisstruktur für dedizierte Hosts ist unten zusammengefasst und schließt die Komponenten vCPU, Arbeitsspeicher, lokalen Speicher und Uplink-Port-Geschwindigkeit ein, da Instanzen auf dedizierten Hosts bereitgestellt werden.

Für dedizierte Hosts sind zusätzlich lokale Speicherplatten auf dem ersten, zweiten, dritten, vierten und fünften Datenträger verfügbar. Auf jedem sekundären Datenträger steht eine zusätzliche Kapazität von 400 GB zur Verfügung.

Instanzen auf Stundenbasis können auf Hosts mit einer Abrechnung auf Monats- oder Stundenbasis bereitgestellt werden. Instanzen auf Monatsbasis können nur auf Hosts mit einer Abrechnung auf Monatsbasis bereitgestellt werden.

| Hostkonfiguration | vCPU	| RAM (GB) | Lokaler Speicher (TB SSD) |	Preis pro Stunde | Preis pro Monat |
| ------------------ | ---- | -------- | ---------------------- | ------------ | ------------- |
| 56x242x1.2 TB	     |  56 	|   242    |        	1,2	          |     $ 3,164   | 	$ 2.099,00    |
{: caption="Tabelle 1. Preisstruktur für dedizierte Hosts" caption-side="top"}

Beachten Sie, dass der Preis je nach Region variiert.

SAN (ans Netz angeschlossen), Premium-Betriebssysteme und Software-Add-ons werden stündlich oder monatlich nach Instanz abgerechnet (abhängig von der auf dem dedizierten Host bereitgestellten Instanz). Die Preisstruktur für diese Komponenten entspricht dem bestehenden Angebot für öffentliche Instanzen und dedizierte Instanzen.

Beispiel: Eine dedizierte Instanz, die auf einem dedizierten Host mit der folgenden Konfiguration bereitgestellt ist, wird nicht nach Instanz abgerechnet. vCPU, Arbeitsspeicher, lokaler Speicher und Uplink-Port-Geschwindigkeiten sind in den Gebühren für den dedizierten Host enthalten.

* 8 vCPU
* 16 GB Arbeitsspeicher (RAM)
* 100 GB auf lokalem SSD als primärer Datenträger
* 400 GB auf lokalem SSD als sekundärer Datenträger
* 400 GB auf lokalem SSD als dritter Datenträger
* 1 Gb/s für öffentliche und private Netz-Uplinks (dedizierter Host)
