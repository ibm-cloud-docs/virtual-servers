---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Feature für das Aussetzen der Abrechnung anzeigen
{: #viewing-suspend-billing-feature}

## Vorbereitungen
Navigieren Sie zuerst zum Einheitenmenü und stellen Sie sicher, dass Sie über die korrekten Kontoberechtigungen verfügen, um die Task auszuführen. 

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie in [Zu Einheiten navigieren](/docs/vsi?topic=virtual-servers-navigating-devices).
* Vergewissern Sie sich, dass Sie über alle erforderlichen Kontoberechtigungen und Zugriff auf die Einheiten verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** der klassischen Infrastruktur kann die Berechtigungen anpassen. 

Weitere Informationen zu Berechtigungen finden Sie in [Berechtigungen für klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Einheitenzugriff verwalten](/docs/vsi?topic=virtual-servers-managing-device-access).

## Feature für das Aussetzen der Abrechnung anzeigen 
Führen Sie die folgenden Schritte aus, um festzustellen, ob Ihre virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt:

1. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus. 
2. Klicken Sie in der **Einheitenliste** auf den Namen der virtuellen Serverinstanz. 
3. Im Abschnitt **Instanzdetails** können Sie feststellen, ob Ihre virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt. 

| Feld                                 | Wert                     |
| --------------------------------------| ------------------------- |
| Ausgesetzte Abrechnung: Aktiviert beim Ausschalten | Feature wird unterstützt.     |
| Ausgesetzte Abrechnung: Nicht verfügbar          | Feature wird nicht unterstützt. |
{: caption="Tabelle 1. Details zum Aussetzen der Abrechnung" caption-side="top"}

## Feature für das Aussetzen der Abrechnung über die SoftLayer-API anzeigen

Der folgende Befehl ist eine Beispielanforderung, mit der über die {{site.data.keyword.slapi_short}} verifiziert wird, ob die virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt.

Bei der folgenden JSON-Anforderung und -Antwort handelt es sich um ein generisches Beispiel.
{:note}

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

JSON-Beispielantwort auf die Anforderung:

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

Weitere Informationen finden Sie in der [SLDN-API-Dokumentation ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}.

## Nächste Schritte

Weitere Informationen zum Feature für das Aussetzen der Abrechnung finden Sie hier:
1. [Abrechnung aussetzen](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [Virtuelle Server verwalten](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

