---



copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Portgeschwindigkeit in Windows erhöhen (Upgrade)

Die Standardportgeschwindigkeit für Kundenserver (sowohl für öffentliche als auch private Netze) beträgt 10 Mbps. Wenn Sie Ihre Portgeschwindigkeit auf 100 Mbps oder 1000 Mbps erhöhen möchten, öffnen Sie ein Ticket mit der Anforderung. Der Vertrieb bittet Sie, die Mindestgebühr zu bestätigen, und ein Techniker ändert die Portgeschwindigkeiten für Ihr Netz.

Führen Sie auf Ihrem Server eine feste Codierung der entsprechenden Netzschnittstellen durch, nachdem das Upgrade auf der Netzseite durchgeführt wurde.

Führen Sie die folgenden Schritte durch, um die Portgeschwindigkeit auf einem Windows-Server zu erzwingen. **Hinweis:** Stellen Sie die Verbindung zu Ihrem Server immer in dem Netz her, an dem Sie gerade NICHT arbeiten, sodass Sie sich nicht selbst aus dem Server aussperren.

1. Wählen Sie **Start > Systemsteuerung > Netzwerkverbindungen** aus.
2. Klicken Sie auf die Netzverbindung, für die Sie ein Upgrade/Downgrade durchführen möchten.
  * Wählen Sie für Upgrades für öffentliche Ports **LAN-Verbindung 2** ODER **Front-End** aus.
  * Wählen Sie für Upgrades für private Ports **LAN-Verbindung** ODER **Back-End** aus.
3. Prüfen Sie im Verbindungsstatusfenster, dass es sich bei der von Ihnen ausgewählten Netzkarte um den Port handelt, für den Sie ein Upgrade durchführen möchten.
4. Wählen Sie die Unterstützungsregisterkarte aus (beachten Sie die IP-Adresse):
  * Bei Upgrades für öffentliche Ports sollte die IP-Adresse eine öffentliche IP-Adresse sein.
  * Bei Upgrades für private Ports sollte die IP-Adresse eine '10.x.x.x'-Adresse sein.
5. Wenn die IP-Adressen nicht zusammenpassen, wiederholen Sie die Schritte 1 bis 3 für die andere Netzverbindung.

## LAN-Status

Wählen Sie erneut die Registerkarte **Allgemein** und dann **Eigenschaften** aus. Ein neues Fenster wird angezeigt.

Wählen Sie in der Registerkarte **Allgemein** des Fensters **Verbindungseigenschaften** **Konfigurieren** aus. Das Treibereigenschaftenfenster wird angezeigt.

1. Wählen Sie die Registerkarte **Erweitert** aus.
2. Wählen Sie **Übertragungsrate&Duplex** in der Eigenschaftsliste aus.
3. Wählen Sie rechts die Registerkarte **Wert** aus und legen Sie die Portgeschwindigkeit, für die Sie ein Upgrade durchführen, mit Vollduplex fest:
  1. Auswahl für 10 MBS: 10Mbps/Voll
  2. Auswahl für 100 MBS: 100Mbps/Voll
  3. Auswahl für 1000 MBS: Auto
4. Klicken Sie auf 'OK'.  

Dadurch beginnt der Server sofort mit der Verwendung der neuen Geschwindigkeit, sodass die Verbindung möglicherweise kurz getrennt wird, während sie neu eingerichtet wird.
