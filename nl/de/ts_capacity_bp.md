---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Hinweise zu Ressourcen für virtuelle Serverinstanzen
{: #capacity-considerations}

## Problem

Wenn Sie einen virtuellen Server bereitstellen, wird möglicherweise die folgende Fehlernachricht ausgegeben:

```
There is insufficient capacity to complete the request.
```
{:screen}

Wenn die Bereitstellung fehlschlägt, schlagen alle virtuellen Serverinstanzen innerhalb der betreffenden Anforderung fehl.
{:tip}

## Ursache

Ein Fehler tritt auf, wenn im Router oder im Rechenzentrum nicht genügend Ressourcen für die Ausführung der Leistungsanforderung verfügbar sind. Es gibt eine Reihe von möglichen Ursachen für diesen Fehler. Die Ressourcenverfügbarkeit ändert sich häufig, sodass Sie möglicherweise warten und es später erneut versuchen möchten.

## Lösung

Sie können mithilfe der folgenden Strategien die Bereitstellung erneut versuchen:

1. Bereitstellung mit Angabe eines anderen Routers.  
2. Bereitstellung ohne Angabe eines Routers.
3. Bereitstellung in einem anderen Rechenzentrum.
4. Bereitstellung von weniger Instanzen.
5. Verteilung der Instanzen durch Bereitstellung in mehreren Rechenzentren.
6. Bereitstellung geringerer Instanzgrößen.
7. Änderung des VSI-Speichers von 'SAN' auf 'Lokal' bzw. 'Lokal' auf 'SAN'.
