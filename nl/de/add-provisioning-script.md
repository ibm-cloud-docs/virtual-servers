---
copyright:
  years: 2014, 2017
lastupdated: "2017-12-21"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Bereitstellungsscript verwalten

Mit Bereitstellungsscripts können Benutzer eine URL für ein Script angeben, das in einer neu bereitgestellten Einheit ausgeführt werden soll. Es gibt keine Beschränkungen für den Scriptnamen; zur Identifizierung der Scripts ist es jedoch einfacher, wenn für die einzelnen Scripts ähnliche Namenskonventionen verwendet werden. Bereitstellungsscripts muss ein vollständig qualifizierter Domänenname zugeordnet werden und auf sie muss der Zugriff mithilfe des Protokolls HTTP oder HTTPS möglich sein. Der verwendete Protokolltyp hat Auswirkung auf die automatische Antwort des Systems, wenn das Bereitstellungsscript in die Einheit heruntergeladen wird.

* Bei Verwendung des **HTTP-Protokolls** ist ein Administrator erforderlich, der das Script nach dem Herunterladen manuell ausführt.
* Bei Verwendung des **HTTPS-Protokolls** wird das Script (falls möglich) automatisch heruntergeladen und installiert. Wenn die URL nicht einem ausführbaren Script zugeordnet ist, wird das Script heruntergeladen und es muss keine weitere Aktion ausgeführt werden.

## Auf Anzeige für Bereitstellungsscripts zugreifen
1. Geben Sie das [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen ein.
2. Wählen Sie in der Navigation die Optionen für **Einheiten > Verwalten > Bereitstellungsscripts** aus, um auf die Anzeige für Bereitstellungsscripts zuzugreifen.


## Bereitstellungsscript hinzufügen

1. Klicken Sie in der Anzeige für **Bereitstellungsscripts** im {{site.data.keyword.slportal}} auf **Bereitstellungsscript hinzufügen** oben in der Anzeige.
* Geben Sie für das Bereitstellungsscript einen **identifizierenden Namen** im Feld **Name** ein.
* Geben Sie den **vollständig qualifizierten Domänennamen**, der dem Script zugeordnet ist, im Feld **URL** ein.
* Klicken Sie auf **Hinzufügen**, um das Bereitstellungsscript zum Konto hinzuzufügen. Klicken Sie auf **Abbrechen**, um den Vorgang abzubrechen.

## Details des Bereitstellungsscripts bearbeiten

1. Klicken Sie in der Anzeige für **Bereitstellungsscripts** im {{site.data.keyword.slportal}} auf eine beliebige Stelle in der Spalte **Name** oder **URL**, damit das Bereitstellungsscript das Script zur Bearbeitung öffnet.
3. Aktualisieren Sie den Namen oder die URL.
  * **Hinweis:** Beim Aktualisieren einer URL müssen Sie einen vollständig qualifizierten Domänennamen verwenden, sonst wird die Änderung nicht gespeichert.
4. Klicken Sie auf eine beliebige Stelle in der Anzeige, um die Bearbeitung zu speichern.

## Nächste Schritte

Bereitstellungsscripts, die einem Konto zugeordnet sind, können jederzeit geändert oder entfernt werden. Bereitstellungsscripts werden solange im {{site.data.keyword.slportal}} gespeichert, bis sie entfernt werden, und sie können jedem neuen Gerät zugeordnet werden, das über das {{site.data.keyword.slportal}} bestellt wird. Wenn dem Script eine HTTP-URL zugeordnet ist, wird es während der Bereitstellung in das neue Gerät heruntergeladen. Scripts, denen HTTPS-URLs zugeordnet sind, werden heruntergeladen und, falls zutreffend, im neuen Gerät ausgeführt.

Nach der Bearbeitung eines Scripts werden gültige Aktualisierungen sofort auf dem Bildschirm angezeigt. Änderungen, die an vorhandenen Bereitstellungsscripts vorgenommen werden, haben keine Auswirkung auf bereits bereitgestellte Geräte.
