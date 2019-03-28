---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Angepasstes Bereitstellungsscript hinzufügen
{: #adding-post-script}

Angepasste Bereitstellungsscripts bieten Benutzern die Möglichkeit, eine URL für ein Script anzugeben, das in einer neu bereitgestellten Einheit ausgeführt werden soll. Angepasste Bereitstellungsscripts können Sie im {{site.data.keyword.slportal_full}} posten und verwalten.
{:shortdesc}

Beim Bestellen einer Einheit können Sie ein angepasstes Bereitstellungsscript auswählen, sofern es in der Anzeige für Bereitstellungsscripts im {{site.data.keyword.slportal}} gepostet wurde. Wenn kein Script hinzugefügt wurde, können Sie eine URL angeben. Als Bereitstellungsscript kann jede Datei verwendet werden, die vom Betriebssystem ausgeführt werden kann (dazu gehören auch kombinierte Binärdateien und alle vom Betriebssystem unterstützten Sprachen). Führen Sie die folgenden Schritte aus, um ein angepasstes Bereitstellungsscript im {{site.data.keyword.slportal}} hinzuzufügen.

**Hinweis:** Diese Funktion ist gegenwärtig nur für Linux- und Unix-basierte Betriebssysteme verfügbar.

## Bereitstellungsscript hinzufügen

1. Wählen Sie im Menü **Einheiten** im [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} die Option **Verwalten** > **Bereitstellungsscripts** aus.
2. Klicken Sie Auf **Bereitstellungsscript hinzufügen**.
4. Geben Sie im Namensfeld einen eindeutigen Namen für das Script ein.
5. Geben Sie im Feld für die URL die URL ein, die dem Script zugeordnet werden soll.
6. Klicken Sie auf **Hinzufügen**.

## Nächste Schritte
Nach dem Absenden einer Bestellung, die ein Bereitstellungsscript beinhaltet, wird die betreffende Einheit wie jede andere Einheit bereitgestellt. Bevor die Einheit verfügbar gemacht wird, wird das angegebene Script in die Einheit heruntergeladen. Die Quelle des Bereitstellungsscripts legt das Ausführungsverhalten für diesen letzten Schritt des Bereitstellungsvorgangs fest. Wenn das Script von einer HTTPS-URL stammt, wird es heruntergeladen und ohne weitere Interaktion des Benutzers ausgeführt. Wenn das Script über HTTP bereitgestellt wurde, wird es nur heruntergeladen. In diesem Fall muss sich der Administrator bei der Einheit anmelden und das Script manuell ausführen.
