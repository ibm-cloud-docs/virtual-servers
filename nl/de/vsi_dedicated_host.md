---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-10"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dedizierte Hosts und dedizierte Instanzen 

Dedizierte Hosts sind virtuelle Server, die Ihnen ermöglichen, das Rechenzentrum und den POD anzugeben, in die der Host platziert werden soll. Anschließend können Sie Instanzen (virtuelle Maschinen) einem bestimmten Host zuweisen, um maximale Kontrolle über die Verteilung von Workloads und flexible Optionen für die Bereitstellungskosten zu haben.
{:shortdesc}

## Garantierte Kapazität
Sie verfügen über eine garantierte Kapazität in dem Rechenzentrum und dem POD, in dem sich Ihr Host befindet. Beispiel: Wenn die Kapazität des PODs ausgeschöpft ist, der Ihren dedizierten Host und die dedizierten Instanzen enthält, können Sie weitere dedizierte Instanzen für Ihren Host zuweisen, wenn der Hostbereich dies zulässt.

## Sichtbarkeit der Workloads
Sie können die gesamte Ressourcenauslastung für alle dedizierten Instanzen, die einem dedizierten Host zugeordnet sind, auf einer Seite anzeigen. Zeigen Sie die Auslastung von Core, Arbeitsspeicher und lokalem Speicher an, um leichter entscheiden zu können, ob dedizierte Instanzen auf einen anderen dedizierten Host migriert werden müssen. Diese Granularitätsebene gibt Ihnen maximale Kontrolle bei der Verwaltung Ihrer Workloads. 

## Verwaltung nach der Bereitstellung
Neben der garantierten Kapazität und der Sichtbarkeit Ihrer Workloads können Sie Ihre dedizierten Instanzen zwischen dedizierten Hosts migrieren, um maximale Kontrolle über die Platzierung der Workloads zu erzielen.

## Wartung
In einigen Fällen ist für die Wartung der Infrastruktur ein dedizierter Host für den Neustart erforderlich. Der Xen-Hypervisor benötigt zum Beispiel eine Aktualisierung. Wenn Sie über mehrere dedizierte Hosts verfügen, haben Sie folgende Optionen, um Ausfallzeiten bei der Wartung zu minimieren. 
* Die Wartung wird von PODs im selben Rechenzentrum übernommen. Sie können Ihre dedizierten Hosts auf separaten PODs bereitstellen, um die erforderliche Wartung zu verteilen. 
* Sie können ein Support-Ticket für einen dedizierten Host erstellen, um anzufordern, dass eine planmäßige Wartung später erfolgt. Während dieser Zeit können Sie dedizierte Instanzen (offline) zwischen dedizierten Hosts im selben POD migrieren.

## Hochverfügbarkeit
Wenn ein dedizierter Host fehlschlägt, wird die Workload auf diesem Host automatisch auf einen neuen dedizierten Host migriert. Dedizierte Instanzen bleiben während des Lebenszyklus des virtuellen Servers dediziert.

In Hochverfügbarkeitsszenarien sollten Sie möglicherweise in Erwägung ziehen, einen zusätzlichen dedizierten Host zu bezeichnen. Der zusätzliche dedizierte Host bietet Ihnen die Flexibilität, um Workloads für Wartungszeiten zu migrieren.
