---



copyright:
  years: 2015, 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Aggiunta di un script di provisioning personalizzato 
{: #adding-post-script}

Gli script di provisioning personalizzati consentono agli utenti di specificare un URL in uno script in esecuzione in un dispositivo di cui è appena stato eseguito il provisioning. Puoi pubblicare e gestire gli script di provisioning personalizzati nel {{site.data.keyword.slportal_full}}.
{:shortdesc}

Quando ordini un dispositivo, puoi selezionare uno script di provisioning personalizzato se è stato pubblicato nella schermata degli script di provisioning del {{site.data.keyword.slportal}}. Se non è stato aggiunto uno script, puoi utilizzare un URL. Gli script di provisioning possono essere un qualsiasi file che può essere eseguito dal sistema operativo (SO), inclusi i file binari combinati o qualsiasi linguaggio supportato dal SO. Utilizza la seguente procedura per aggiungere uno script di provisioning personalizzato nel {{site.data.keyword.slportal}}.

**Nota:** questa funzione è al momento disponibile solo per sistemi operativi Linux e basati su Unix.

## Aggiunta di un script di provisioning

1. Dal menu **Dispositivi** nel [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window}, seleziona **Gestisci** > **Script di provisioning**.
2. Fai clic su **Aggiungi script di provisioning**.
4. Nel campo del nome, immetti un nome dello script univoco.
5. Nel campo dell'URL, immetti l'URL esatto da associare allo script.
6. Fai clic su **Aggiungi**.

## Passi successivi
Dopo aver inviato un ordine che contiene uno script di provisioning, viene eseguito il provisioning del dispositivo in modo simile a qualsiasi altro dispositivo. Prima che il dispositivo diventi disponibile, lo script specificato viene scaricato nel dispositivo. L'origine dello script di provisioning determina il comportamento durante quest'ultimo passo del processo di provisioning. Se lo script viene fornito da un URL HTTPS, viene scaricato ed eseguito con nessuna ulteriore interazione richiesta dall'utente. Se lo script viene fornito tramite HTTP, viene soltanto scaricato. Per gli script forniti tramite HTTP, l'amministratore deve accedere al dispositivo ed eseguire lo script manualmente.
