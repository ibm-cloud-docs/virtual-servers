---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-06"

subcollection: virtual-servers

---

{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Speicheroptionen
{: #storage-options}

Sie können für jeden virtuellen Server zwischen SAN-Speicher (portierbar) und lokalem Speicher wählen. Der SAN-Speicher bzw. der lokale Speicher kann nach Bedarf durch weitere Produkte ergänzt werden.

## Lokaler Speicher

Der lokale Speicher befindet sich auf lokalen Platten für den virtuellen Server-Host. Der lokale Speicher ermöglicht schnellere Lese- und Schreibzugriffe auf die Platten. Die Platten bilden eine RAID-Konfiguration (RAID = Redundant Array of Independent Disks), die Redundanz, Datenträgeraustausch und Statusüberwachung ermöglicht und vollständig von {{site.data.keyword.cloud}} verwaltet wird. In neueren Rechenzentren werden für diesen Speichertyp ausschließlich Solid-State-Laufwerke (SSDs) verwendet, um eine optimale Leistung zu erzielen.

## Portierbarer SAN-Speicher

Portierbare Speicherdatenträger sind Zusatzspeicherlösungen, die ausschließlich in {{site.data.keyword.BluVirtServers_short}} verfügbar sind.  Der portierbare SAN-Speicher basiert auf den Flashspeicherclustern von {{site.data.keyword.cloud_notm}}, nicht auf dem lokalen Hostspeicher. Diese Infrastruktur bietet eine höhere Ausfallsicherheit bei Hostausfällen und kann deutlich größere Volumen unterstützen. Bei einem Hostausfall werden virtuelle Serverinstanzen, die den SAN-Speicher nutzen, automatisch auf andere Hosts migriert und neu gestartet.

Portierbarer Speicher stellt eine ideale Lösung dar, wenn Sie Daten, die in einem beliebigen Rechenzentrum im {{site.data.keyword.cloud_notm}}-Netz vorhanden sind, zwischen virtuellen Servern übertragen möchten. Portierbare Speicherdatenträger sind nützlich für Datenbankanwendungen, für die Zugriff auf rohen, unformatierten Blockspeicher erforderlich ist und zum Verschieben großer Dateien zwischen {{site.data.keyword.BluVirtServers_short}}.

Alle sekundären Platten werden als portierbarer Speicher angehängt. In den meisten Fällen können diese sekundären Platten jederzeit abgehängt werden, um das Verschieben auf andere virtuelle Server zu ermöglichen.

Bei öffentlichen virtuellen Servern, die ausgeglichenen lokalen Speicher verwenden, können primäre oder sekundäre Platten nicht abgehängt werden.
{:important}

Die Platten können erneut an einen anderen Server angehängt werden, sofern die Änderung nicht das Plattenkontingent oder die maximale Datenträgergröße des virtuellen Zielservers überschreitet.

Die verschobene Platte wird an den Speichertyp des Zielservers angepasst.
{:note}

Wenn ein portierbarer Speicherdatenträger an einen virtuellen Server in einem anderen Rechenzentrum als der ursprüngliche virtuelle Server angehängt ist, kopiert das interne {{site.data.keyword.cloud_notm}}-System den Datenträger in das SAN im neuen Rechenzentrum. Das System überprüft daraufhin die Integrität des kopierten Datenträgers und entfernt den ursprünglichen portierbaren Datenträger aus dem ursprünglichen Rechenzentrum-SAN.

## Beschränkungen für LVM

LVM (Logical Volume Management, logische Datenträgerverwaltung) wird nicht als bootfähiges Partitionierungsschema unterstützt. Bei Unterstützung und entsprechender Konfiguration des Betriebssystems können sekundäre Platten in virtuellen Servern für LVM-Partitionen verwendet werden. LVM ist jedoch kein unterstütztes Dateisystem für Imagevorlagen oder flexible Images.

## Ergänzender Speicher

Virtuelle Server sind vollständig kompatibel mit {{site.data.keyword.filestorage_short}}, {{site.data.keyword.blockstorageshort}} und {{site.data.keyword.cos_full}}. Diese Speichertypen werden für Clusterlaufwerke, gemeinsam genutzten Dateispeicher, Archivspeicher sowie für umfangreiche Speicheranforderungen oder spezifische Leistungsanforderungen empfohlen.

Weitere Informationen zu Optionen mit ergänzendem Speicher finden Sie in den folgenden Ressourcen:

* [Einführung in Blockspeicher](/docs/infrastructure/BlockStorage?topic=BlockStorage-getting-started)
* [Einführung in Dateispeicher](/docs/infrastructure/FileStorage?topic=FileStorage-getting-started)
* [Einführung in Objektspeicher](/docs/services/cloud-object-storage?topic=cloud-object-storage-getting-started)

## Nächste Schritte
Weitere Informationen zur Verwendung von portierbaren Speicherdatenträgern finden Sie unter den folgenden Tasks:
* [Portierbaren Speicher verwalten](/docs/vsi?topic=virtual-servers-accessing-portable-storage#accessing-portable-storage)
* [Beschreibung für portierbaren Speicher bearbeiten](/docs/vsi?topic=virtual-servers-editing-a-portable-storage-description#editing-a-portable-storage-description)
