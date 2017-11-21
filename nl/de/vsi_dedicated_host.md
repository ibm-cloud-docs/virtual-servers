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


# Dedizierte Hosts und dedizierte Instanzen 

Dedizierte Hosts sind virtuelle Server, für die Sie angeben können, in welchem Rechenzentrum und POD der Host platziert werden soll. Anschließend können Sie Instanzen (virtuelle Maschinen) einem bestimmten Host zuweisen, um maximale Kontrolle über die Verteilung von Workloads und flexible Optionen für die Kostenbereitstellung zu erzielen.
{:shortdesc}

## Garantierte Kapazität
Sie verfügen über eine garantierte Kapazität in dem Rechenzentrum und dem POD, in dem sich Ihr Host befindet. Beispiel: Wenn die Kapazität des PODs ausgeschöpft ist, der Ihren dedizierten Host und die dedizierten Instanzen enthält, können Sie weitere dedizierte Instanzen für Ihren Host zuweisen, wenn der Hostbereich dies zulässt.

## Sichtbarkeit der Workloads
Sie können die gesamte Ressourcenauslastung für alle dedizierten Instanzen, die einem dedizierten Host zugeordnet sind, auf einer Seite anzeigen. Zeigen Sie die Auslastung von Kern, Arbeitsspeicher und lokalem Speicher an, um leichter entscheiden zu können, ob dedizierte Instanzen auf einen anderen dedizierten Host migriert werden müssen. Diese Granularitätsebene gibt Ihnen maximale Kontrolle bei der Verwaltung Ihrer Workloads. 

## Verwaltung nach der Bereitstellung
Neben der garantierten Kapazität und der Sichtbarkeit Ihrer Workloads können Sie Ihre dedizierten Instanzen zwischen dedizierten Hosts migrieren, um maximale Kontrolle über die Platzierung der Workloads zu erzielen.
