---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informationen zu portierbaren Speicherdatenträgern

Portierbare Speicherdatenträger sind Zusatzspeicherlösungen, die ausschließlich in {{site.data.keyword.BluVirtServers_short}} verfügbar sind. Sie können jeweils mit einem virtuellen Server verbunden werden. Sie stellen ferner eine ideale Lösung dar, wenn Sie Daten, die in einem beliebigen Rechenzentrum im {{site.data.keyword.cloud}}-Netz vorhanden sind, zwischen virtuellen Servern übertragen möchten. Portierbare Speicherdatenträger sind nützlich für Datenbankanwendungen, für die Zugriff auf rohen, unformatierten Blockspeicher erforderlich ist und zum Verschieben großer Dateien zwischen {{site.data.keyword.BluVirtServers_short}}.

Wenn ein portierbarer Speicherdatenträger an einen virtuellen Server in einem anderen Rechenzentrum als der ursprüngliche virtuelle Server angehängt ist, kopiert das interne {{site.data.keyword.cloud}}-System den Datenträger in das SAN im neuen Rechenzentrum. Das System überprüft daraufhin die Integrität des kopierten Datenträgers und entfernt den ursprünglichen portierbaren Datenträger aus dem ursprünglichen Rechenzentrum-SAN.

## Nächste Schritte
Weitere Informationen zur Verwendung von portierbaren Speicherdatenträgern finden Sie unter den folgenden Tasks:
* [Auf portierbaren Speicher zugreifen](../storage/access-portable-storage-screen.html)
* [Beschreibung für portierbaren Speicher bearbeiten](../storage/edit-description-portable-storage-volume-psv.html)
