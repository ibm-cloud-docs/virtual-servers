---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# Häufig gestellte Fragen: Virtuelle Server  
{: #faqs-virtual-servers}

## Welche Typen von virtuellen Servern können verwendet werden?
{: faq}
{{site.data.keyword.BluSoftlayer_full}} bietet verschiedene Typen virtueller Server in der klassischen Infrastruktur an. Das Standardangebot ist ein öffentlich zugänglicher virtueller Server, d. h. eine Multi-Tenant-Konfiguration, die sich für eine Vielzahl von Anforderungen eignet. Wenn Sie nach einer Einzel-Tenant-Konfiguration suchen, sollten Sie das Angebot für dedizierte virtuelle Server in Betracht ziehen. Dieses Angebot eignet sich speziell für Anwendungen mit streng festgelegtem Ressourcenbedarf. Weitere Informationen zu den aktuellen Angeboten für virtuelle Server finden Sie unter [Einführung in virtuelle Server](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers).

IBM Cloud bietet die VPC-Infrastruktur (VPC = Virtual Private Cloud), bei der es sich um die Cloudplattform der nächsten Generation handelt. Sie erstellen einen eigenen Bereich in {{site.data.keyword.cloud_notm}}, um über VPC eine isolierte Umgebung in der öffentlichen Cloud auszuführen. VPC bietet die Sicherheit einer privaten Cloud und die Flexibilität und einfache Verwendbarkeit einer öffentlichen Cloud. Weitere Informationen hierzu finden Sie im Abschnitt mit den [Informationen zur virtuellen privaten Cloud](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about).

## Wo finde ich Preisinformationen zu öffentlichen Instanztypen?
{: faq}

Preisinformationen finden Sie unter [Eigenen virtuellen Server erstellen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud/virtual-servers){: new_window}.

## Wo finde ich Preisinformationen zu öffentlichen virtuellen Instanzen?
{: faq}

Bei der Einschätzung der Kosten für einen {{site.data.keyword.cloud_notm}}-Server, mit dem Ihre Workload unterstützt werden soll, müssen Sie im [{{site.data.keyword.cloud_notm}}-Katalog](https://cloud.ibm.com/catalog) beginnen. Wählen Sie im Katalog **Berechnen** und dann den Servertyp 'Bare Metal Server', 'Virtual Server' oder 'Virtual Server for VPC (Virtual Private Cloud)' aus. Informationen zur Preisstruktur finden Sie im Abschnitt zur [Berechnungsfunktion für die Bereitstellung virtueller Server ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

## Kann ich Plattenspeicherplatz zu meinem virtuellen Server mit stündlicher oder monatlicher Abrechnung hinzufügen?
{: faq}

Sie können ein Upgrade oder Downgrade für den Plattenspeicherplatz jedes beliebigen virtuellen Servers durchführen, indem Sie die Speicheroptionen in den Feldern *Erster Datenträger* bis *Fünfter Datenträger* in der Anzeige *Konfiguration* für die gewünschte Einheit aktualisieren. Weitere Informationen finden Sie unter [Vorhandenen virtuellen Server neu konfigurieren](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).

## Wie viele virtuelle Server mit stündlicher Abrechnung kann ich starten?
{: #concurrent}
{: faq}

Die Anzahl der Instanzen, die ausgeführt werden können, hängt vom Reifegrad Ihres Kontos ab. Standardmäßig gilt für Konten, die älter als 45 Tage sind, eine Obergrenze von 20 Instanzen, die auf öffentlichen virtuellen Servern, dedizierten virtuellen Servern und Bare Metal Server-Systemen gleichzeitig ausgeführt werden können. Für ein neueres Konto gilt ein niedrigerer Grenzwert. Wenn Sie diesen Grenzwert erhöhen möchten, wenden Sie sich an den Support und geben Sie dabei an, welche Aktionen Sie ausführen möchten und wie viele gleichzeitig ausgeführte Instanzen Sie benötigen.

## Wie wird die Bandbreite für meine auf Stundenbasis abgerechneten virtuellen Server in Rechnung gestellt?
{: faq}

Bei der stundenbasierten Abrechnung für virtuelle Komponenten wird zwischen eingehendem und ausgehendem Datenverkehr unterschieden. Der gesamte eingehende Datenverkehr für Ihren virtuellen Server ist gebührenfrei. Der ausgehende Datenverkehr wird gemessen und pro GB abgerechnet. Dabei werden die Gesamtsummen jeweils am Ende Ihres Abrechnungszeitraums ermittelt.

## In welchen Fällen wird mein virtueller Server auf einen anderen Host migriert?
{: faq}

In wenigen Fällen muss ein virtueller Server möglicherweise auf einen anderen Host migriert werden. Falls eine Migration erforderlich ist, wird der virtuelle Server beendet, migriert und anschließend erneut gestartet. Ein virtueller Server wird möglicherweise in den folgenden Fällen migriert:

* Ein Hypervisor muss aktualisiert werden, ein Host wird stillgelegt oder ein Host darf keine neuen Instanzen annehmen. Wenn ein Host für eine dieser Änderungen markiert ist, wird bei einem Warmstart einer seiner virtuellen Server über die {{site.data.keyword.cloud_notm}}-Konsole automatisch die Migration des virtuellen Servers auf einen anderen Host ausgelöst.
* Wartung der Infrastruktur. Sie erhalten möglicherweise eine E-Mail mit der Information, dass auf einem System, das als Host für Ihren virtuellen Server dient, eine Wartung erforderlich ist. Ihr virtueller Server muss im Zuge der Infrastrukturwartung möglicherweise migriert werden.
* Upgrade auf eine vorhandene Instanz. Um konsistente Leistung zu erzielen wird bei einem Upgrade einer Instanz diese möglicherweise auf einen anderen Host migriert um sicherzustellen, dass sie die geeignete dedizierte CPU und den geeigneten Speicher erhält.
* Ein dedizierter Host schlägt fehl. Dedizierte Instanzen werden auf einen anderen leeren Host migriert, ohne vorhandene Kapazitäten zu verwenden, über die Sie möglicherweise verfügen.

In einem Wartungsfenster wird möglicherweise die Option **Host migrieren** im Menü **Aktionen** Ihrer Einheit in der {{site.data.keyword.cloud_notm}}-Konsole angezeigt. Mit der Option **Host migrieren** können Sie den virtuellen Server im Wartungszeitraum bei Gelegenheit auf einen neuen Host migrieren. Wenn Sie die Migration nicht im Wartungszeitraum einleiten, wird der virtuelle Server automatisch migriert, um die erforderliche Wartung abzuschließen. Die Option **Host migrieren** bleibt nicht dauerhaft bestehen und ist nur während der Wartungszeiträume verfügbar, die über Wartungsbenachrichtigungen kommuniziert werden.

Die Option **Host migrieren** wird möglicherweise auch dann angezeigt, wenn einer Ihrer virtuellen Server eine bestimmte Hypervisorstufe aufweisen muss, die auf dem aktuellen Host nicht verfügbar ist.

## Was geschieht mit meinen Daten, wenn mein portierbarer Speicher gelöscht wird?
{: faq}

Wenn Speicher gelöscht wird, werden alle Zeiger auf die Daten auf diesem Datenträger entfernt, sodass auf die Daten nicht mehr zugegriffen werden kann. Wenn der physische Speicher dann einem anderen Konto bereitgestellt wird, werden neue Zeiger zugeordnet. Es gibt für das neue Konto keine Möglichkeit, auf Daten zuzugreifen, die sich auf der physischen Speichereinheit befunden haben mögen. Alle neuen Zeiger enthalten nur Nullen. Wenn neue Daten auf den Datenträger/die LUN geschrieben werden, werden alle noch vorhandenen Daten, auf die nicht mehr zugegriffen werden kann, überschrieben.

## Kann ich ein Red Hat Cloud Access-Abonnement zum Erstellen eines virtuellen Servers verwenden?
{: faq}

Ja. Beim Importieren eines Images können Sie angeben, dass Sie die Betriebssystemlizenz bereitstellen werden. Weitere Informationen finden Sie unter [Red Hat Cloud Access verwenden](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription). Anschließend können Sie einen virtuellen Server von dieser Imagevorlage bestellen und Ihr bestehendes Abonnement von [Red Hat Cloud Access ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window} verwenden.

## Worin besteht der Unterschied zwischen einem virtuellen Server und einem virtuellen privaten Server (VPS)?
{: faq}

Ein virtueller Server entspricht weitgehend dem Konzept des virtuellen privaten Servers (VPS) oder des virtuellen dedizierten Servers (VDS), mit dem Sie bereits vertraut sind. Diese virtuellen Serverumgebungen bieten die Möglichkeit zum Bereitstellen separater, privater und geschützter Umgebungen auf einem einzigen Hardwareknoten. Dabei ist der Funktionsumfang von VDS und VPS etwas stärker eingeschränkt. VPS- und VDS-Optionen sind im Allgemeinen auf eine Einzelserverarchitektur beschränkt. Die einzigen Ressourcen, die hinzugefügt oder zwischen den einzelnen virtuellen Servern in einer VDS- oder VPS-Konfiguration aufgeteilt werden können, sind die Ressourcen, die physisch auf diesem einzelnen Server installiert wurden.

Virtuelle Server werden in einer Cloudarchitektur mit mehreren Servern bereitgestellt, die alle verfügbaren Hardwareressourcen zusammenfasst und für die Verwendung durch einzelne Instanzen bereitstellt. Virtuelle Server können auf eine gemeinsam genutzte, SAN-basierte primäre Speicherplattform mit hoher Kapazität oder auf leistungsstarken lokalen Festplattenspeicher zurückgreifen. Da jede Instanz Teil der größeren Cloudumgebung ist, erfolgt die Kommunikation zwischen allen virtuellen Servern nahezu ohne Verzögerung.

## Warum wird bei der Bereitstellung eines virtuellen Servers ein Kapazitätsfehler ausgegeben?
{: faq}

Wenn Sie einen virtuellen Server bereitstellen, wird möglicherweise eine Fehlernachricht ausgegeben, in der Sie informiert werden, dass die Kapazität für die Ausführung der Anforderung nicht ausreicht. Wenn die Bereitstellung fehlschlägt, schlagen alle virtuellen Serverinstanzen innerhalb der betreffenden Anforderung fehl. Ein Kapazitätsfehler tritt auf, wenn im Router oder im Rechenzentrum nicht genügend Ressourcen für die Ausführung der Leistungsanforderung verfügbar sind. Es gibt eine Reihe von möglichen Ursachen für diesen Fehler. Die Ressourcenverfügbarkeit ändert sich häufig, sodass Sie möglicherweise warten und es später erneut versuchen möchten. Weitere Informationen über Strategien zur Vermeidung dieses Fehlers finden Sie in [Hinweise zu Ressourcen für virtuelle Serverinstanzen](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).

## Wie melde ich mich bei meinem Server an?
{: faq}

Melden Sie sich an der Konsole an und navigieren Sie zum Menü **Einheiten**. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices). Wählen Sie in der **Einheitenliste** Ihre Instanz aus. Sie können die Benutzernamen und Kennwörter der Einheit, die zur Anmeldung verwendet werden, anzeigen und verwalten. Weitere Informationen hierzu finden Sie im Abschnitt zum [Anzeigen und Verwalten von Benutzernamen und Kennwörtern für Einheiten](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device). 

## Wie kann ich VPN verwenden, um auf das private IBM Cloud-Netz zuzugreifen?
{: faq}

Die Anmeldung beim VPN kann über die [Webschnittstelle](https://www.softlayer.com/VPN-Access){: external} oder über einen [eigenständigen VPN-Client](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients) für Linux, macOS oder Windows durchgeführt werden. Weitere Informationen zu den Aktionen, die nach der Herstellung der Verbindung zum VPN ausgeführt werden müssen, finden Sie im Abschnitt zur [Verwendung des SSL-VPN](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn).

## Wie kann ich für meinen virtuellen Server einen Warmstart durchführen?
{: faq}

Warmstarts von Einheiten können sowohl über die **Einheitenliste** als auch über die Snapshot-Ansicht einer einzelnen Instanz durchgeführt werden. Navigieren Sie in der **Einheitenliste** in Ihrer Konsole zu der gewünschten virtuellen Serverinstanz. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices). Wählen Sie für die Einheit, die Sie verwalten möchten, die Option **Aktionen** und anschließend **Neu starten** aus.

## Wie kann ich den Rescue-Kernel nutzen?
{: faq}

Das Booten in den Rescue-Kernel kann hilfreich sein, wenn auf dem Server ein Problem aufgetreten ist. Zum Starten des Rescue-Kernels müssen Sie den Einheitennamen in der **Einheitenliste** in Ihrer Konsole auswählen. Wählen Sie im Menü **Aktionen** die Option **Rescue-Modus** oder für eine Windows-Instanz die Option **Vom Image booten** aus. Weitere Informationen finden Sie im Abschnitt zum [Starten des Rescue-Kernels](/docs/vsi?topic=virtual-servers-launching-rescue).

## Wo kann ich den Netzstatus abfragen?
{: faq}

Sie können die Seite **Status** direkt unter [{{site.data.keyword.cloud_notm}} - Status](https://cloud.ibm.com/status){: external} aufrufen, um den aktuellen Status der Ressourcen an allen {{site.data.keyword.cloud_notm}}-Standorten anzuzeigen. Sie können die Liste filtern, indem Sie spezielle Komponenten und Standorte auswählen (z. B. Virtual Server-Systeme auswählen und die Netzkonnektivität anzeigen).

## Wie kann ich einen Compliance-Bericht anfordern?
{: faq}

Informationen zum Anzeigen oder Anfordern von Compliance-Informationen einschließlich SOC-Berichten finden Sie im Abschnitt [Wie kann ich feststellen, ob meine Daten sicher sind?](/docs/overview?topic=overview-security).

