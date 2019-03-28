---

copyright:
  years: 2014, 2018
lastupdated: "2018-04-27"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gestione di uno script di provisioning
{: #managing-a-provisioning-script}

Utilizza gli script di provisioning per specificare un URL di uno script da eseguire su un dispositivo di cui è appena stato eseguito il provisioning. Non hai limitazioni per il nome dello script; tuttavia, l'utilizzo di una convezione di denominazione simile per ogni script rende più facile l'identificazione. Gli script di provisioning devono essere associati a un nome del dominio completo e accessibili utilizzando i protocolli HTTP e HTTPS. Il tipo di protocollo utilizzato influenza la risposta automatizzata del sistema quando viene scaricato lo script di provisioning sul dispositivo.

* L'utilizzo del **protocollo HTTP** richiede che un amministratore esegua lo script manualmente dopo che è stato scaricato.
* L'utilizzo del **protocollo HTTPS** scarica ed esegue lo script automaticamente, se possibile. Se l'URL non è associato a uno script eseguibile, lo script viene scaricato e non deve essere effettuata alcuna altra azione.

## Accesso alla schermata degli script di provisioning
1. Immetti [{{site.data.keyword.slportal_full}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} con le tue credenziali univoche.
2. Seleziona **Dispositivi > Gestisci > Script di provisioning** dalla navigazione per accedere alla schermata degli script di provisioning.


## Aggiunta di uno script di provisioning
{: #add-provisioning-script}

1. Dalla schermata **Script di provisioning** in {{site.data.keyword.slportal}}, fai clic su **Aggiungi script di provisioning** all'inizio della schermata.
* Immetti un **nome di identificazione** per lo script di provisioning nel campo **Nome**.
* Immetti il **nome del dominio completo** associato allo script nel campo **URL**.
* Fai clic su **Aggiungi** per aggiungere lo script di provisioning all'account. Fai clic su **Annulla** per annullare l'azione.

## Modifica dei dettagli dello script di provisioning

1. Dalla schermata **Script di provisioning** in {{site.data.keyword.slportal}}, fai clic in un qualsiasi punto nella colonna **Nome** o **URL** dello script di provisioning per aprire lo script per la modifica.
3. Aggiorna il nome o l'URL.
  * **Nota:** quando aggiorni un URL, devi utilizzare un nome del dominio completo o la modifica non viene salvata.
4. Fai clic in un qualsiasi punto nella schermata per salvare la modifica.

## Passi successivi

Gli script di provisioning associati a un account possono essere modificati o rimossi in qualsiasi momento. Gli script di provisioning vengono salvati in {{site.data.keyword.slportal}} finché non vengono rimossi e possono essere associati a un nuovo dispositivo ordinato tramite il {{site.data.keyword.slportal}}. Se lo script viene associato a un URL HTTP, viene scaricato nel nuovo dispositivo durante il provisioning. Gli script associati agli URL HTTP vengono scaricati e, quando applicabile, eseguiti nel nuovo dispositivo.

Dopo aver modificato uno script, gli aggiornamenti validi vengono visualizzati nella schermata immediatamente. Le modifiche apportate agli script di provisioning esistenti non influenzano i dispositivi già forniti.
