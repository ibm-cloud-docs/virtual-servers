---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# FAQs: Virtuelle Server  

## Welche Typen von virtuellen Servern können verwendet werden?
{{site.data.keyword.BluSoftlayer_full}} bietet verschiedene Typen virtueller Server an. Das Standardangebot ist ein öffentlich zugänglicher virtueller Server, d. h. eine Multi-Tenant-Konfiguration, die sich für eine Vielzahl von Anforderungen eignet. Wenn Sie nach einer Einzel-Tenant-Konfiguration suchen, sollten Sie das Angebot für dedizierte virtuelle Server in Betracht ziehen. Dieses Angebot eignet sich speziell für Anwendungen mit streng festgelegtem Ressourcenbedarf. Weitere Informationen zu den aktuellen Angeboten für virtuelle Server finden Sie unter [Einführung in virtuelle Server](../vsi/vsi_index.html).

## Wo finde ich Preisinformationen zu öffentlichen Instanztypen?
Preisinformationen finden Sie unter [Eigenen virtuellen Server erstellen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers){: new_window}.

## Kann ich Datenträger zu meinem virtuellen Server auf Stunden- oder Monatsbasis hinzufügen?
Sie können ein Upgrade oder Downgrade für die Datenträger jedes beliebigen virtuellen Servers durchführen, indem Sie die Speicheroptionen in den Feldern *Erster Datenträger* bis *Fünfter Datenträger* in der Anzeige *Konfiguration* für die gewünschte Einheit ändern. Weitere Informationen finden Sie unter [Vorhandenen virtuellen Server neu konfigurieren](../vsi/vsi_reconfigure.html).

## Wie viele auf Stundenbasis abgerechnete virtuelle Server kann ich starten?

Für das Konto gilt eine Obergrenze von 20 Instanzen, die auf öffentlichen virtuellen Servern, dedizierten virtuellen Servern und Bare-Metal-Servern gleichzeitig ausgeführt werden können.  Wenn Sie diese Obergrenze erweitern möchten, wenden Sie sich an den Support und geben Sie dabei an, was Sie beabsichtigen und wie viele gleichzeitig ausgeführte Instanzen Sie benötigen.

## Wie wird die Bandbreite für meine auf Stundenbasis abgerechneten virtuellen Server in Rechnung gestellt?

Bei der stundenbasierten Abrechnung für virtuelle Komponenten wird zwischen eingehendem und ausgehendem Datenverkehr unterschieden. Der gesamte eingehende Datenverkehr für Ihren virtuellen Server ist gebührenfrei. Der ausgehende Datenverkehr wird gemessen und pro GB abgerechnet. Dabei werden die Gesamtsummen jeweils am Ende Ihres Abrechnungszeitraums ermittelt.

## In welchen Fällen wird mein virtueller Server auf einen anderen Host migriert?

In wenigen Fällen muss ein virtueller Server möglicherweise auf einen anderen Host migriert werden. Falls eine Migration erforderlich ist, wird der virtuelle Server beendet, migriert und anschließend erneut gestartet. Ein virtueller Server wird möglicherweise in den folgenden Fällen migriert:

* Ein Hypervisor muss aktualisiert werden, ein Host wird stillgelegt oder ein Host darf keine neuen Instanzen annehmen. Wenn ein Host für eine dieser Änderungen markiert ist, wird bei einem Warmstart einer seiner virtuellen Server vom {{site.data.keyword.slportal_full}} automatisch das Migrieren des virtuellen Servers auf einen anderen Host ausgelöst.
* Wartung der Infrastruktur. Sie erhalten möglicherweise eine E-Mail mit der Information, dass auf einem System, das als Host für Ihren virtuellen Server dient, eine Wartung erforderlich ist. Ihr virtueller Server muss im Zuge der Infrastrukturwartung möglicherweise migriert werden.
* Upgrade auf eine vorhandene Instanz. Um konsistente Leistung zu erzielen wird bei einem Upgrade einer Instanz diese möglicherweise auf einen anderen Host migriert um sicherzustellen, dass sie die geeignete dedizierte CPU und den geeigneten Speicher erhält.

In einem Wartungsfenster wird möglicherweise die Option **Host migrieren** im Menü **Aktionen** Ihrer Einheit im {{site.data.keyword.slportal}} angezeigt. Mit der Option **Host migrieren** können Sie den virtuellen Server im Wartungszeitraum bei Gelegenheit auf einen neuen Host migrieren. Wenn Sie die Migration nicht im Wartungszeitraum einleiten, wird der virtuelle Server automatisch migriert, um die erforderliche Wartung abzuschließen. Die Option **Host migrieren** bleibt nicht dauerhaft bestehen und ist nur während der Wartungszeiträume verfügbar, die über Wartungsbenachrichtigungen kommuniziert werden.

Die Option **Host migrieren** wird möglicherweise auch dann angezeigt, wenn einer Ihrer virtuellen Server eine bestimmte Hypervisorstufe aufweisen muss, die auf dem aktuellen Host nicht verfügbar ist.

## Was geschieht mit meinen Daten, wenn mein portierbarer Speicher gelöscht wird?

Wenn Speicher gelöscht wird, werden alle Zeiger für die Daten auf dem Datenträger entfernt, das heißt auf die Daten kann nicht mehr zugegriffen werden. Wenn die physische Speichereinheit dann einem anderen Konto bereitgestellt wird, werden neue Zeiger zugeordnet. Es gibt für das neue Konto keine Möglichkeit, auf Daten zuzugreifen, die sich auf der physischen Speichereinheit befunden haben mögen. Alle neuen Zeiger enthalten nur Nullen. Wenn neue Daten auf den Datenträger/die LUN geschrieben werden, werden alle noch vorhandenen Daten, auf die nicht mehr zugegriffen werden kann, überschrieben.

## Kann ich ein Red Hat Cloud Access-Abonnement zum Erstellen eines virtuellen Servers verwenden?

Ja. Beim Importieren eines Images können Sie angeben, dass Sie die Betriebssystemlizenz bereitstellen werden. Weitere Informationen finden Sie unter [Red Hat Cloud Access verwenden](../infrastructure/image-templates/use-red-hat-cloud-access.html). Anschließend können Sie einen virtuellen Server von dieser Imagevorlage bestellen und Ihr bestehendes Abonnement von [Red Hat Cloud Access ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} verwenden.

## Worin besteht der Unterschied zwischen einem virtuellen Server und einem virtuellen privaten Server (VPS)?

Ein virtueller Server entspricht weitgehend dem Konzept des virtuellen privaten Servers (VPS) oder des virtuellen dedizierten Servers (VDS), mit dem Sie bereits vertraut sind. Diese virtuellen Serverumgebungen bieten die Möglichkeit zum Bereitstellen separater, privater und geschützter Umgebungen auf einem einzigen Hardwareknoten. Dabei ist der Funktionsumfang von VDS und VPS etwas stärker eingeschränkt. VPS- und VDS-Optionen sind im Allgemeinen auf eine Einzelserverarchitektur beschränkt, das heißt nur die physisch auf dem Einzelserver installierten Ressourcen können zwischen den einzelnen virtuellen Servern auf einem VDS oder VPS hinzugefügt oder aufgeteilt werden.

Virtuelle Server werden in einer Cloudarchitektur mit mehreren Servern bereitgestellt, die alle verfügbaren Hardwareressourcen zusammenfasst und für die Verwendung durch einzelne Instanzen bereitstellt. Virtuelle Server können auf eine gemeinsam genutzte, SAN-basierte primäre Speicherplattform mit hoher Leistung oder auf leistungsstarken lokalen Festplattenspeicher zurückgreifen. Da jede Instanz Teil der größeren Cloudumgebung ist, erfolgt die Kommunikation zwischen allen virtuellen Servern nahezu ohne Verzögerung.

## Es kann keine Verbindung zur Virtualisierungs-API hergestellt werden. Wie kann ich dieses Problem beheben?

Dieser Fehler tritt in der Regel auf, weil ein Kennwort abgelaufen ist. Beheben Sie diesen Fehler, indem Sie das Root- oder Administratorkennwort für das Betriebssystem des virtuellen Servers im {{site.data.keyword.slportal_full}} aktualisieren.
