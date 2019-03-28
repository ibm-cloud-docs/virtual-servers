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
{:faq: data-hd-content-type='faq'}


# Häufig gestellte Fragen (FAQs): Dedizierte Hosts und Instanzen
{: #faqs-dedicated-hosts-and-instances}

## Was ist ein dedizierter Host?
{:faq}

Dedizierte {{site.data.keyword.Bluemix}}-Hosts sind physische Server, die einer Benutzergruppe zugeordnet sind. Dedizierte Hosts stellen Kapazität zum Bereitstellen virtueller Server bereit und ermöglichen maximale Kontrolle über die Platzierung.

## Welche Vorteile bieten dedizierte Hosts im Vergleich zu dedizierten Instanzen?
{:faq}

Beide Angebote bieten garantierte Einzel-Tenant-Funktionalität. Dedizierte Hosts bieten neben der Flexibilität zum Angeben des Hosts, auf dem dedizierte Hostinstanzen bereitgestellt werden sollen, die folgenden Vorteile:
   * Kontrolle darüber, in welchem {{site.data.keyword.cloud}}-Rechenzentrum der Server platziert wird
   * Flexible Verwaltung Ihrer Server bei geänderten Workload-Anforderungen (z. B. Migrieren der virtuellen Server zwischen Ihren dedizierten Hosts im selben POD)

## Kann ich meine dedizierten Instanzen beibehalten, oder muss ich einen dedizierten Host und dedizierte Hostinstanzen einrichten?
{:faq}

Ja, Sie können Ihre vorhandenen dedizierten Instanzen beibehalten.

## Kann ich zwischen der Bereitstellung (automatisch zugeordneter) dedizierter Instanzen und dedizierter Hostinstanzen wechseln?
{:faq}

Nein. Vorhandene, automatisch zugeordnete Instanzen können nicht auf dedizierten Hostinstanzen erneut bereitgestellt werden. Wenn Sie die Platzierung virtueller Server benötigen, müssen Sie diese als dedizierte Hostinstanzen auf dedizierten Hosts bereitstellen.

## Welcher Servertyp (virtueller Server oder Bare-Metal-Server) unterstützt das Angebot für dedizierte Hosts?
{:faq}

Das Angebot wird auf virtuellen Servern unterstützt. ({{site.data.keyword.Bluemix_notm}} bietet keine Bare-Metal-Server an.) Virtuelle Hosts und Bare-Metal-Server unterscheiden sich in der Vorlaufzeit bis zur Bereitstellung und in der Verwaltung der Virtualisierung.

## Wie sieht der Lebenszyklus bis zur Bereitstellung eines dedizierten Hosts aus?
{:faq}

Dedizierte Hosts werden bei der Bereitstellung bestimmten Benutzern zugeordnet. Die Zuordnung zum Benutzerkonto bleibt bestehen, bis sie aufgehoben wird. Dedizierte Hosts werden ausschließlich mit bedarfsgesteuerter Preisgestaltung (mit stündlicher oder monatlicher Abrechnung) angeboten, d. h. wenn sie aufgehoben werden, greifen die Abrechnungsmodelle der anderen Angebote für die {{site.data.keyword.BluSoftlayer_full}} auf Stunden- oder Monatsbasis.

## Wie wird das Angebot für dedizierte Hosts abgerechnet?
{:faq}

Sie können dedizierte Hosts nach Bedarf mit stündlicher oder monatlicher Abrechnung erwerben. Auf Hosts, die stundenweise abgerechnet werden, können Instanzen mit monatlicher *und* mit stündlicher Abrechnung bereitgestellt werden. Die Preise für dedizierte Hosts beinhalten Core, RAM, lokalen SSD-Speicher und Netzportgeschwindigkeiten. Premium-Betriebssysteme, SAN-Speicher (SAN = Storage Area Network) sowie Preise und Lizenzen für Software-Add-ons werden entsprechend der auf dem dedizierten Host bereitgestellten Instanz (auf Stunden- oder Monatsbasis) abgerechnet. Auf diese Angebote wird dasselbe Preismodell angewendet wie auf öffentliche und dedizierte {{site.data.keyword.Bluemix_notm}}-Instanzen.

## Ich arbeite mit einem bedarfsgesteuerten dedizierten Host. Wie wird dieser Host abgerechnet?
{:faq}

Die stündliche oder monatliche bedarfsgesteuerte Gebühr für dedizierte Hosts wird in Rechnung gestellt. Für dedizierte Hostinstanzen, die auf dedizierten Hosts bereitgestellt werden, können Instanzgebühren anfallen, wie in der Antwort auf die FAQ **Wie wird das Angebot für dedizierte Hosts abgerechnet?** angegeben.

## Wie wird die Tenant-Konfiguration beim Bereitstellen dedizierter Hosts und dedizierter Hostinstanzen angegeben?
{:faq}

Die Tenant-Standardeinstellung für dedizierte Instanzen ist die Einzel-Tenant-Konfiguration. Sie können dedizierte Instanzen wahlweise auf einem dedizierten Host (dedizierte Hostinstanzen) bereitstellen oder auf einem automatisch zugewiesenen Host (dedizierte Instanzen). Dedizierte Instanzen auf automatisch zugewiesenen Hosts stellen nicht dieselbe Verwaltungsebene bereit wie dedizierte Instanzen auf einem dedizierten Host.

## Kann ich verschiedene Konfigurationen für dedizierte Hostinstanzen auf meinem dedizierten Host beliebig kombinieren?
{:faq}

Ja. Sie können virtuelle Server mit verschiedenen Größen auf dedizierten Hosts bereitstellen, solange die Kapazitätsobergrenze des jeweiligen Hosts eingehalten wird.

## Wie kann ich erkennen, wie viele dedizierte Hostinstanzen auf jedem dedizierten Host ausgeführt werden können?
{:faq}

Jeder dedizierte Host verfügt über eine bestimmte Obergrenze für den Core, den Arbeitsspeicher und den lokalen SSD-Speicher. Anhand der Ressourcenzuordnungen, die auf der Registerkarte 'Zuordnungen' angezeigt werden, können Sie erkennen, wie viele dedizierte Hostinstanzen bereitgestellt werden, welche Hostkapazität aktuell genutzt wird und welche Kapazität verfügbar ist.

## Welche Images können auf dedizierten Hosts bereitgestellt werden?
{:faq}

Sie können entsprechend den Festlegungen in der Drittanbietervereinbarung Archiv-Images für virtuelle {{site.data.keyword.Bluemix_notm}}-Server bereitstellen oder eigene Images importieren.

## Gibt es eine Obergrenze für die Anzahl der dedizierten Hosts, die einem einzelnen Konto zugeordnet werden können?
{:faq}

Ja, für jedes Konto gelten die Ressourcengrenzwerte, die für alle {{site.data.keyword.BluSoftlayer_notm}} as a Service-Ressourcen definiert sind. Sie können mehrere Bestellungen für jedes Konto aufgeben, jedoch maximal zwei dedizierte Hosts pro Bereitstellungsbestellung.

## Kann die maximale Anzahl der Bereitstellungen auf dedizierten Hosts überschritten werden?
{:faq}

Nein. Auf dedizierten Hosts kann nicht mehr als die aufgelistete Kapazität bereitgestellt werden.
