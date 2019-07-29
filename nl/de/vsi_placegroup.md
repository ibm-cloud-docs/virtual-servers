---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Platzierungsgruppen
{: #placement-groups}

Hohe Verfügbarkeit (High Availability, HA) ist ein wichtiger Aspekt bei jeder Cloudbereitstellung. Unabhängig davon, ob es sich um die Website Ihres E-Commerce-Unternehmens oder um eine Produktionsdatenbank handelt, die von der wichtigsten Anwendung Ihres Unternehmens genutzt wird, ist es von übergeordneter Bedeutung, dass der unterbrechungsfreie Service jederzeit gewährleistet bleiben muss. Um dieses Ziel zu erreichen, stellt die Entwicklung robuster Infrastrukturen einen Faktor dar, der für die IT Architect-Clients oberste Priorität hat, um so die Verfügbarkeitszeiten kontinuierlich zu verbessern. Obwohl die Verfügbarkeitszeiten eines Systems in IT-Organisationen streng überwacht werden, können diese unter die relevanten Grenzen fallen oder es kann zu erheblichen Ausfallzeiten kommen, die für das gesamte Unternehmen ein erhebliches Problem darstellen. 

Durch die Implementierung von redundanten Systemen auf jeder Ebene Ihrer Infrastruktur können Single Points of Failure (SPOF) eliminiert werden. Dieses Ziel stellt einen entscheidenden Faktor für die Erzielung guter Werte für diese Metrik dar. Für Workloads, die auf virtuellen Servern ausgeführt werden, bedeutet dies, dass Failover-Lösungen mit mehreren virtuellen Servern implementiert werden müssen, die automatisch die Aufgaben der anderen Server übernehmen können, wenn ein Absturz auftritt.

Allerdings kann nicht verlässlich festgestellt werden, wo diese Einheiten relativ zueinander platziert werden sollten, sofern Ihre öffentlichen virtuellen Server nicht in unterschiedlichen Rechenzentren bereitgestellt werden. Diese Tatsache kann zu Problemen führen, wenn Sie 1) eine HA-Konfiguration aufbauen wollen und wenn 2) Ihre virtuellen Server auf demselben physischen Host platziert werden, sodass eine Schwachstelle entstehen kann, wenn eine einzelne Hardwarekomponente ausfällt. Obwohl dies wenig wahrscheinlich ist, verfügen IT-Manager nicht über die Möglichkeit, einen SPOF für kritische Anwendungen herzustellen. Die Verwendung mehrerer Rechenzentren stellt eine Option zur Lösung dieses Problems dar, hierdurch kann es jedoch zur Entstehung spezieller Herausforderungen kommen, die den Einsatz zusätzlicher Appliances erfordern oder zu erhöhten Latenzzeiten führen. Dies gilt insbesondere in Regionen, in denen lediglich ein Rechenzentrum zur Verfügung steht.

Das Design von Platzierungsgruppen für virtuelle Server in {{site.data.keyword.cloud}} ermöglicht die Lösung dieses Problems. Platzierungsgruppen bieten eine Möglichkeit zur Steuerung des Hosts, auf dem ein neuer öffentlicher virtueller Server platziert wird. Im aktuellen Release ist eine Verteilungsregel enthalten, die vorgibt, dass virtuelle Server in einer Platzierungsgruppe alle auf unterschiedliche Hosts verteilt werden. Sie können eine Hochverfügbarkeitsanwendung in einem Rechenzentrum erstellen und wissen dabei, dass Ihre virtuellen Server voneinander isoliert sind.

Platzierungsgruppen mit der Verteilungsregel stehen zur Verfügung, um die Erstellung in den ausgewählten {{site.data.keyword.cloud_notm}}-Rechenzentren durchzuführen. Nach der Erstellung können Sie einen neuen virtuellen Server in dieser Gruppe bereitstellen und sicherstellen, dass dieser virtuelle Server sich nicht auf demselben Host wie einer Ihrer anderen virtuellen Server befindet. Der größte Vorteil dieser Lösung besteht darin, dass für die Nutzung dieser Funktion keinerlei Gebühren anfallen. Bei Verfügbarkeit stellen die {{site.data.keyword.cloud_notm}}-Platzierungsgruppen für virtuelle Server eine kostenlose Funktion dar. 

Sie können die Platzierungsgruppe erstellen und anschließend bis zu fünf neue virtuelle Serverinstanzen zuweisen. Mit der Verteilungsregel werden alle virtuellen Server auf unterschiedlichen physischen Hosts bereitgestellt.

## Nächste Schritte

Informationen zum Erstellen und Verwalten neuer Platzierungsgruppen finden Sie in [Platzierungsgruppen verwalten](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup#vsi_managing_placegroup).
