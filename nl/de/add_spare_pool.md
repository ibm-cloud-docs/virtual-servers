---



copyright:
  years: 2014, 2018
lastupdated: "2018-02-09"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Ersatzpools hinzufügen 
{: #adding-spare-pools}

Die Verwendung von Ersatzpools ist eine Form des Failover, bei der bestimmte Einheiten als Hot-Spare-Einheiten vorgesehen werden und den Workflow einer primären Einheit übernehmen können, wenn diese fehlschlägt. Damit eine Einheit als Hot-Spare-Einheit vorgesehen werden kann, muss sie dem Ersatzpool hinzugefügt und einer primären Einheit zugeordnet werden. Führen Sie die folgenden Schritte aus, um dem Ersatzpool eine Einheit hinzuzufügen.
{:shortdesc}

## Ersatzpools hinzufügen

1. Öffnen Sie das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window}, indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Wählen Sie in der Navigationsleiste **Einheiten > Ersatzpool** aus, um die Anzeige *Ersatzpool* aufzurufen.
3. Klicken Sie auf den Link **Zum Ersatzpool hinzufügen**.
   
   Eine Liste wird mit auswählbaren Einheiten gefüllt, die dem Ersatzpool hinzugefügt werden können.{:tip}
   
4. Wählen Sie die Einheiten aus, die dem Ersatzpool hinzugefügt werden sollen.
5. Klicken Sie auf **Ausgewählte Einheiten hinzufügen**.
6. Klicken Sie auf **Bestätigung**, um die Einheiten dem Ersatzpool hinzuzufügen. 

## Nächste Schritte
Nachdem die Übertragung einer Einheit in den Ersatzpool gestartet wurde, wird die Einheit innerhalb einer Stunde in den Ersatzpool übertragen. Nachdem die Einheit im Ersatzpool aktiv ist, wird sie in der Ersatzpoolanzeige angezeigt und kann als Hot-Spare-Einheit für eine primäre Einheit vorgesehen werden.
