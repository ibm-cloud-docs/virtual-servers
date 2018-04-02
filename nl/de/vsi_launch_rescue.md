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


# Rescue-Kernel starten 
{: #launching-rescue}

Der Rescue-Kernel ist eine Live-Rescue-Umgebung, die dem Kunden die Möglichkeit gibt, einen Bare-Metal-Server oder einen virtuellen Server online zu schalten, um Systemprobleme zu beheben, die sonst nur durch erneutes Laden des Betriebssystems behoben werden können. Der Rescue-Kernel muss im {{site.data.keyword.slportal_full}} aufgerufen werden. Führen Sie die folgenden Schritte aus, um den Rescue-Kernel für eine Einheit zu starten.
{:shortdesc}

## Rescue-Kernel starten

1. Öffnen Sie das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/), indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Klicken Sie in der Einheitenliste auf den Namen der Einheit, für die Sie den Rescue-Kernel starten möchten.
3. Klicken Sie auf die Dropdown-Liste *Aktionen* in der rechten oberen Ecke und wählen Sie **Rescue** aus.
4. Klicken Sie auf die Schaltfläche **Ja**, um für Ihre Einheit sofort den Rescue-Kernel zu starten. Klicken Sie auf die Schaltfläche **Nein**, um die Aktion abzubrechen.

## Nächste Schritte
Nach dem Starten des Rescue-Kernels wird die Einheit ausgeschaltet und im Rescue-Kernel für das Betriebssystem der Einheit erneut gestartet. Dieser Vorgang kann mehrere Minuten dauern.

Der Fernzugriff auf die Einheit ist über die IP-Adresse der Einheit möglich. Sie können auf die Einheit im Rescue-Kernel zugreifen, indem Sie die Root- oder Administratorberechtigungsnachweise für die Einheiten angeben, die im {{site.data.keyword.slportal}} aufgezeichnet sind. Bei Verwendung des Rescue-Kernels können Sie nach Fehlern suchen sowie Probleme erkennen und beheben wie auf einer regulär gestarteten Einheit. Falls erforderlich, können Sie im Rescue-Kernel-Betriebssystem Laufwerke anhängen. Um den Rescue-Kernel zu beenden und Ihre Einheit wieder in die normale Umgebung zu versetzen, führen Sie für die Einheit einen Warmstart über das {{site.data.keyword.slportal}} oder das Rescue-Kernel-Betriebssystem durch.

Weitere Informationen zum erneuten Starten einer Einheit finden Sie unter [Virtuelle Server verwalten](../vsi/vsi_managing.html).

