---



copyright:
  years: 2018
lastupdated: "2018-10-31"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Gruppi di posizionamento

Con i gruppi di posizionamento per {{site.data.keyword.BluVirtServers}}, puoi usare le istanze pubbliche per eseguire attività di sviluppo per l'alta disponibilità in un data center oppure fornire un livello aggiuntivo di tolleranza dell'errore all'interno di una distribuzione più ampia.
{:shortdesc}

Crea il tuo gruppo di posizionamento e assegna quindi fino a 5 nuove istanze del server virtuale. Con la regola di diffusione, il provisioning di ciascuno dei server virtuali viene eseguito su host fisici differenti.

Per iniziare, attieniti alla seguente procedura:
 
1. Dal tuo browser, apri [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){:new_window} ed esegui l'accesso al tuo account.
2. Nella pagina Placement Groups, fai clic su **Add Placement Group**.
3. Immetti un nome, una descrizione e un data center per il gruppo di posizionamento e fai clic su **Add**.
4. Individua la sezione **Order** e fai clic su **Devices**.
5. Nella pagina Devices, fai clic su **Hourly** o **Monthly** per una delle offerte del Virtual Server.
6. Completa qualsiasi altra informazione necessaria e fai clic su **Add to Order**. Viene aperta la pagina Checkout.
7. Puoi selezionare qualsiasi gruppo di posizionamento esistente. **Spread** significa che le istanze sono su hardware fisico differente.
8. Infine, fai clic su **Submit Order**.

##Limitazioni
Le istanze esistenti non possono essere aggiunte a un gruppo di posizionamento; puoi aggiungere un'istanza del server virtuale a un gruppo di posizionamento solo in fase di provisioning. 

Per rimuovere un'istanza da un gruppo di posizionamento, devi eliminare o recuperare l'istanza.
     
## Passi successivi

Per creare e gestire nuovi gruppi di posizionamento, vedi [Gestione dei gruppi di posizionamento](vsi_managing_placegroup.html).
