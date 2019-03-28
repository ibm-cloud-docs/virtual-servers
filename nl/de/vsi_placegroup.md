---

copyright:
  years: 2018
lastupdated: "2018-10-31"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Platzierungsgruppen
{: #placement-groups}

Mit Platzierungsgruppen für {{site.data.keyword.BluVirtServers}} können Sie öffentliche Instanzen für einen Build mit hoher Verfügbarkeit in einem Rechenzentrum verwenden oder eine zusätzliche Fehlertoleranzebene innerhalb einer größeren Bereitstellung einrichten.
{:shortdesc}

Erstellen Sie die Platzierungsgruppe und weisen Sie dann bis zu 5 neue virtuelle Serverinstanz zu. Auf der Basis der Verteilungsregel wird jeder der virtuellen Server auf einem anderen physischen Host bereitgestellt.

Führen Sie zunächst diese Schritte aus:

1. Öffnen Sie [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){:new_window} im Browser und melden Sie sich bei Ihrem Konto an.
2. Klicken Sie auf der Seite 'Platzierungsgruppen' auf die Option **Platzierungsgruppe hinzufügen**.
3. Geben Sie einen Namen, eine Beschreibung und ein Rechenzentrum für die Platzierungsgruppe an und klicken Sie auf **Hinzufügen**.
4. Suchen Sie den Bereich **Bestellung** und klicken Sie auf **Einheiten**.
5. Klicken Sie auf der Seite 'Einheiten' auf die Option **Stündlich** oder **Monatlich** für eines der Angebote für virtuelle Server.
6. Geben Sie alle weiteren erforderlichen Informationen an und klicken Sie auf **Zur Bestellung hinzufügen**. Die Check-out-Seite wird angezeigt.
7. Sie können beliebige vorhandene Platzierungsgruppen auswählen. **Verteilen** bedeutet, dass sich die Instanzen auf verschiedenen physischen Hardwarekomponenten befinden.
8. Klicken Sie abschließend auf **Bestellung absenden**.

##Einschränkungen
Vorhandene Instanzen können nicht zu einer Platzierungsgruppe hinzugefügt werden; es ist nur möglich, eine virtuelle Serverinstanz zum Zeitpunkt der Bereitstellung zu einer Platzierungsgruppe hinzuzufügen.

Zum Entfernen einer Instanz von einer Platzierungsgruppe muss die Instanz gelöscht oder freigegeben werden.

## Nächste Schritte

Informationen zum Erstellen und Verwalten neuer Platzierungsgruppen finden Sie in [Platzierungsgruppen verwalten](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup).
