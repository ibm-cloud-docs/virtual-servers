---



copyright:
  years: 2018
lastupdated: "2018-10-30"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Feature für das Aussetzen der Abrechnung anzeigen
Informationen darüber, ob die virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt, können Sie über das {{site.data.keyword.slportal_full}} oder die {{site.data.keyword.slapi_short}} anzeigen.

## Feature für das Aussetzen der Abrechnung im Kundenportal anzeigen
Führen Sie die folgenden Schritte aus, um über das {{site.data.keyword.slportal}} zu ermitteln, ob die virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung:

1. Melden Sie sich beim [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an. 
2. Wählen Sie im Menü **Einheiten** die Option **Einheitenliste** aus. 
3. Klicken Sie in der **Einheitenliste** auf den Namen der virtuellen Serverinstanz. 
4. Auf der Registerkarte **Konfiguration** im Abschnitt **System** können Sie Informationen darüber anzeigen, ob die virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt. 

| Feld                                 | Wert                     |
| --------------------------------------| ------------------------- |
| Ausgesetzte Abrechnung: Aktiviert beim Ausschalten | Feature wird unterstützt.    |
| Ausgesetzte Abrechnung: Nicht verfügbar            | Feature wird nicht unterstützt. |
{: caption="Tabelle 1. Details zum Aussetzen der Abrechnung" caption-side="top"}

## Feature für das Aussetzen der Abrechnung über die SoftLayer-API anzeigen

Der folgende Befehl ist eine Beispielanforderung, mit der über die {{site.data.keyword.slapi_short}} verifiziert wird, ob die virtuelle Serverinstanz das Feature für das Aussetzen der Abrechnung unterstützt.

**Hinweis**: Bei der folgenden JSON-Anforderung und -Antwort handelt es sich um ein generisches Beispiel. 

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
1. [Informationen zum Aussetzen der Abrechnung ](vsi_about_suspend.html)
2. [Virtuelle Server verwalten](vsi_managing.html)
