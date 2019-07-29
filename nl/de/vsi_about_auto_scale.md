---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords: auto scale, virtual servers

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informationen zur automatischen Skalierung
{: #about-auto-scale}

Mithilfe der automatischen Skalierung für virtuelle {{site.data.keyword.cloud}}-Serverinstanzen haben Sie die Möglichkeit, den manuellen Skalierungsprozess zu automatisieren, der mit dem Hinzufügen oder Entfernen von Instanzen zur Unterstützung Ihrer Geschäftsanwendungen verbunden ist. Auf diese Weise können Sie neue Instanzen automatisch einrichten, wenn mehr Ressourcen benötigt werden, und diese Instanzen wieder abschalten und entfernen, wenn die zusätzliche Auslastung wieder abnimmt. Die automatische Skalierung verwendet Gruppen, die die Richtlinien enthalten, mit denen die Erweiterung oder Verkleinerung Ihrer Umgebung durchgeführt wird. Diese Richtlinien verwenden Aktionen, um virtuelle Server auf Basis Ihrer Geschäfts- und Anwendungsanforderungen hinzuzufügen oder zu entfernen.
{:shortdesc}

Die automatische Skalierung verfügt über die folgenden Funktionen: 

* Nahtlose automatische Durchführung eines Scale-up Ihrer Instanzen, wenn zur Erfüllung des Bedarfs weitere Ressourcen erforderlich sind.
* Nahtlose automatische Durchführung eines Scale-down Ihrer Instanzen durch Entfernung nicht mehr benötigter Ressourcen, wenn der Bedarf sinkt (sodass Sie Geld einsparen können).
* Flexible Skalierungsauslöser: CPU-Prozentsatz, öffentliche und private Ausgangsbandbreite sowie öffentliche und private Eingangsbandbreite.
* Echtzeitnahe Statusaktualisierungen für Skalierungsaktivitäten in Gruppen.
* Optionale Integration von virtuellem LAN (VLAN) und lokalen Lastausgleichsfunktionen.

Die automatische Skalierung kann auf zwei allgemeine Geschäftslösungen angewendet werden:

| Lösung   | Beschreibung |
| -------- | ----------- |
| [Zeitplanbasierte Skalierung](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling) | Die zeitplanbasierte Skalierung kann zum Einrichten von Richtlinien für zeitbasierte Nutzungsspitzen wie beispielsweise an Wochenenden oder Feiertagen verwendet werden. Die zeitplanbasierte Skalierung kann eingesetzt werden, wenn ein Unternehmen Datenverkehrsspitzen erwartet. Dies kann z. B. bei einer Social-Networking-Site der Fall sein, die auf Basis eines Zeitplans mehr Ressourcen benötigt. |
| [Ressourcenbasierte Skalierung](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling) | Die ressourcenbasierte Zeitplanung kann zum Einrichten von Richtlinien für unregelmäßig auftretende Auslastungsspitzen auf Basis der Ressourcennutzung verwendet werden. Unregelmäßig auftretende Auslastungsspitzen beim Datenverkehr können auftreten, wenn die Markteinführung eines Produkts durchgeführt wird oder wenn eine E-Commerce-Site eine Verkaufsaktion durchführt, für die Ressourcen benötigt werden, um die Antwortzeiten stabil zu halten. |
{: caption="Tabelle 1. Lösungen für automatische Skalierung" caption-side="top"}

Wenn Sie kein Kontoadministrator sind, muss Ihr Benutzerkonto über die Berechtigung zur Nutzung der automatischen Skalierung verfügen. Der Kontoadministrator kann die Berechtigung eines Benutzers über die {{site.data.keyword.cloud_notm}}-Konsole erteilen. Weitere Informationen zum Aktualisieren von Berechtigungen finden Sie im Abschnitt zum [Einrichten von Benutzerberechtigungen für die automatische Skalierung](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
{:note}


