---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Rescue-Kernel starten
{: #launching-rescue}

Der Rescue-Kernel ist eine Live-Rescue-Umgebung, die Ihnen die Möglichkeit gibt, ein Bare Metal Server-System oder einen virtuellen Server online zu schalten, um Systemprobleme zu beheben, die sonst nur durch erneutes Laden des Betriebssystems behoben werden können. Der Rescue-Kernel muss in der {{site.data.keyword.cloud}}-Konsole aufgerufen werden. Führen Sie die folgenden Schritte aus, um den Rescue-Kernel für eine Einheit zu starten.
{:shortdesc}

## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Tasks auszuführen.

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen.

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Rescue-Kernel starten

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
2. Klicken Sie in der **Einheitenliste** auf den Namen der Einheit, für die Sie den Rescue-Kernel starten möchten.
3. Wählen Sie im Menü *Aktionen* die Option **Rescue-Modus** aus.
4. Klicken Sie auf **Ja**, um für Ihre Einheit sofort den Rescue-Kernel zu starten.

## Rescue-Kernel für eine Windows-Instanz starten

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus.
2. Klicken Sie in der **Einheitenliste** auf den Namen der Einheit, für die Sie den Rescue-Kernel starten möchten.
3. Wählen Sie im Menü *Aktionen* die Option **Vom Image booten** aus.
4. Wählen Sie neben dem öffentlichen Image *WindowsRescueStandalone.iso* die Option für **Aus diesem Image starten** aus.

## Nächste Schritte
Nach dem Starten des Rescue-Kernels wird die Einheit ausgeschaltet und im Rescue-Kernel für das Betriebssystem der Einheit erneut gestartet. Dieser Vorgang kann mehrere Minuten dauern.

Der Fernzugriff auf die Einheit ist über die IP-Adresse der Einheit möglich. Sie können auf die Einheit im Rescue-Kernel zugreifen, indem Sie die Root- oder Administratorberechtigungsnachweise für die Einheiten angeben, die in der {{site.data.keyword.cloud_notm}}-Konsole aufgezeichnet werden. Bei Verwendung des Rescue-Kernels können Sie nach Fehlern suchen sowie Probleme erkennen und beheben wie auf einer regulär gestarteten Einheit. Falls erforderlich, können Sie im Rescue-Kernel-Betriebssystem Laufwerke anhängen. Um den Rescue-Kernel zu beenden und Ihre Einheit wieder in die normale Umgebung zu versetzen, führen Sie für die Einheit einen Warmstart über die {{site.data.keyword.cloud_notm}}-Konsole oder das Rescue-Kernel-Betriebssystem durch.

Weitere Informationen zum erneuten Starten einer Einheit finden Sie unter [Virtuelle Server verwalten](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers).
