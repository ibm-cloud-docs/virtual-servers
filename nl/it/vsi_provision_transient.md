---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-21"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:note: .note}
{:important: .important}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Provisioning delle istanze temporanee
{: #ordering-vs-transient}

## Informazioni preliminari
Hai due opzioni per eseguire il provisioning delle tue istanze del server virtuale temporanee. La prima è attraverso la console {{site.data.keyword.cloud}} e la seconda tramite il {{site.data.keyword.slportal}}. La console e il {{site.data.keyword.slportal}} richiedono ID di accesso univoci. Non puoi utilizzare il tuo nome utente e la tua password della console per accedere al portale e viceversa.
{:shortdesc}

Per la console {{site.data.keyword.cloud_notm}}, devi disporre di un account di cui è stato eseguito l'upgrade per ordinare i server virtuali. Per ulteriori informazioni sull'upgrade del tuo account, consulta [Account Pagamento a consumo](/docs/account?topic=account-accounts#paygo).
{:note}

Prima di iniziare, controlla i seguenti prerequisiti.

  1. Controlla le opzioni di distribuzione disponibili. Per ulteriori informazioni, vedi [Server virtuali temporanei](/docs/vsi?topic=virtual-servers-about-vs-transient).

  2. Controlla le considerazioni sulla capacità dell'istanza del server virtuale.  Per ulteriori informazioni, consulta [Considerazioni sulle risorse per le istanze del server virtuale](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).
  
  3. Apri la pagina [Istanza server virtuale ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/gen1/infrastructure/provision/vs?guestType=transient&cm_sp=Cloud-Product-_-OnPageNav-IBMCloudPlatform_IBMVirtualMachines-_-VSI_Prod_Midpage){: new_window} dalla console {{site.data.keyword.cloud_notm}}.

## Provisioning di un'istanza del server virtuale temporanea
{: #ordering-transient-instance}

Per eseguire il provisioning di un'istanza del server virtuale temporanea, devi prendere in considerazione le seguenti informazioni. 

Devi aver eseguito l'accesso per visualizzare tutte le opzioni disponibili. 
{:tip}

### Istanza temporanea

| Campo    | Dettagli     |
| -------- | ----------- |
| Fatturazione  | Le istanze temporanee sono disponibili solo come istanze orarie. Se annulli la tua istanza oraria dopo 10 giorni, paghi soltanto le ore di tali 10 giorni. |
| Nome host | Può contenere delle etichette composte da caratteri alfanumerici e trattini, separati da punti. Le etichette non possono essere solo numeriche, iniziare o terminare con un trattino né avere trattini o punti consecutivi. |
| Dominio | Deve avere due o più etichette che possono essere composte da caratteri alfanumerici e trattini, separati da punti. Le etichette non possono iniziare o terminare con un trattino o avere trattini o punti consecutivi. L'ultima etichetta deve essere di sole lettere. |
| Gruppo di posizionamento | Puoi selezionare un gruppo di posizionamento per la tua istanza. Se aggiungi un gruppo di posizionamento, la regola di "distribuzione" indica che le istanze si trovano su hardware fisici diversi. Per ulteriori informazioni, vedi [Gruppi di posizionamento ](/docs/vsi?topic=virtual-servers-placement-groups). |
| Ubicazione  | Le ubicazioni sono composte di regioni (aree geografiche specifiche) e zone (data center a tolleranza di errore all'interno di una regione). Seleziona l'ubicazione in cui vuoi venga creata la tua istanza. |
| Profili popolari | Prendi in considerazione di selezionare una delle configurazioni di profilo popolare che supporta i casi di utilizzo più comuni. I profili contengono delle istanze preconfigurate pronte per l'utilizzo in pochi minuti. |
| Tutti i profili |Per ulteriori informazioni sulle opzioni di profilo disponibili per le istanze temporanee, vedi [Server virtuali temporanei](/docs/vsi?topic=virtual-servers-about-vs-transient). |
| Chiavi SSH     | Le chiavi SSH consentono l'accesso a un'istanza senza utilizzare una password dai client corrispondenti per ogni chiave pubblica implementata sull'istanza. Se decidi di aggiungere una chiave SSH, fornisci una chiave pubblica della tua chiave SSH, che puoi utilizzare per accedere alla tua istanza dopo il provisioning. |
| Immagine        |  Un'immagine è il sistema operativo distribuito per la tua istanza. Puoi selezionare alcune opzioni gratuite come CentOS e Ubuntu. Sono anche disponibili opzioni a pagamento come Windows Server e Red Hat Enterprise Linux (RHEL). È importante tenere presente che Windows richiede un disco primario da 100 GB. |
{: caption="Tabella 1. Opzioni istanza temporanea" caption-side="top"}

### Componenti aggiuntivi istanza temporanea 

Se scegli un componente aggiuntivo software, deve essere compatibile con la tua immagine per evitare un errore quando ordini la tua istanza. Ad esempio, non puoi eseguire il provisioning di un'immagine RedHat con un database Microsoft.
{:important}

| Campo     | Dettagli     |
| --------- | ----------- |
| Software del database      | Puoi selezionare un software del database da installare. {{site.data.keyword.cloud_notm}} supporta tutti i software del database distribuiti durante il processo di provisioning. Puoi anche installare il tuo software del database dopo la distribuzione del server. |
| Servizi | Alcuni servizi vengono automaticamente selezionati al tuo posto, a seconda della tua selezione dell'immagine. Puoi scegliere uno qualsiasi dei componenti aggiuntivi del servizio rimanenti per la tua istanza. |
| Script di provisioning | Gli script di provisioning sono comunemente utilizzati per applicare una configurazione specifica del cliente a un server e per agevolare l'automazione della tua strategia di ridimensionamento. Gli script di provisioning possono essere un qualsiasi file che può essere eseguito dal sistema operativo (SO), inclusi i file binari combinati o qualsiasi linguaggio supportato dal SO. Gli script di provisioning non possono essere utilizzati con le immagini cloud-init. Per ulteriori informazioni, vedi [Script di provisioning](/docs/vsi?topic=virtual-servers-provisioning-scripts). |
| Dati utente        | Puoi aggiungere dei dati utente che eseguono automaticamente le attività di configurazione comuni o che eseguono gli script. I dati utente possono essere utilizzati su immagini cloud-init e non cloud-init.  |
{: caption="Tabella 2. Componenti aggiuntivi istanza temporanea" caption-side="top"}

### Dischi di archiviazione collegati

Se hai bisogno di ulteriore archiviazione, puoi collegare dei dischi di archiviazione alla tua istanza. I tipi di dischi di archiviazione disponibili dipendono dal profilo che selezioni. 

### Interfaccia di rete

| Campo    | Dettagli     |
| -------- | ----------- |
| Velocità porta di uplink | Puoi selezionare la velocità uplink per la tua istanza, fino a 1 GB/s. Viene eseguito il backup di questi uplink virtuali da uplink fisici ridondanti nelle reti dedicata e pubblica di IBM. La velocità dedicata e pubblica è sempre la stessa del momento dell'ordine, con l'opzione di eseguire l'upgrade o il downgrade di un uplink se necessario. |
| Gruppo di sicurezza privato e pubblico  | Puoi utilizzare i gruppi di sicurezza per attivare una serie di regole di filtro IP che definiscono come gestire il traffico in entrata e in uscita per le interfacce pubbliche e private della tua istanza. Per ulteriori informazioni, vedi [Informazioni sui gruppi di sicurezza IBM](/docs/infrastructure/security-groups?topic=security-groups-about-ibm-security-groups). |
| VLAN privata e pubblica | La tua istanza del server virtuale viene posizionata, per impostazione predefinita, su una VLAN assegnata automaticamente. Puoi scegliere una diversa VLAN se ne hai già una nel tuo data center selezionato. Per ulteriori informazioni, vedi [Informazioni sulle VLAN](/docs/infrastructure/vlans?topic=vlans-about-vlans). |
| Sottorete privata e pubblica | La selezione di una sottorete è facoltativa e deve essere utilizzata solo quando hai bisogno che il tuo dispositivo utilizzi un indirizzo IP da una sottorete. Se selezioni una sottorete, verifica di avere abbastanza indirizzi IP per completare la richiesta. Se non hai abbastanza indirizzi IP per la tua sottorete, il tuo ordine può essere ritardato o annullato. Per ulteriori informazioni, vedi [Informazioni sulle sottoreti e gli IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
{: caption="Tabella 3. Opzioni dell'interfaccia di rete" caption-side="top"}

### Componenti aggiuntivi dell'interfaccia di rete

| Campo    | Dettagli     |
| -------- | ----------- |
| Larghezza di banda | L'assegnazione della larghezza di banda non è inclusa con le istanze del server virtuale temporanee. |
| Firewall hardware e software  | I servizi firewall impediscono il traffico non desiderato sui tuoi server, riducono il rischio di un attacco e consentono alle tue risorse server di essere dedicate al loro utilizzo previsto. |
| Indirizzo IP primario | Un indirizzo IP primario viene automaticamente assegnato alla tua istanza. |
| Indirizzi IP secondari pubblici | Queste sottoreti sono gestite da te per la durata della tua istanza del server virtuale. Puoi annullare la sottorete separatamente, ma se annulli la tua istanza, viene rimossa anche la sottorete. Per ulteriori informazioni, vedi [Informazioni sulle sottoreti e gli IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips#about-subnets-and-ips). |
| Indirizzi IPv6 e IPv6 statici e pubblici | Puoi selezionare un indirizzo IPv6 on degli indirizzi IPv6 statici e pubblici per la tua istanza. |
| Gestione VPN | Questa opzione viene selezionata automaticamente per la tua istanza con gli utenti VPN SSL illimitati. Per ulteriori informazioni, vedi [Informazioni sulla VPN](/docs/infrastructure/iaas-vpn?topic=VPN-about-iaas-vpn). |
{: caption="Tabella 4. Componenti aggiuntivi dell'interfaccia di rete" caption-side="top"}

## Provisioning delle istanze del server virtuale temporanee tramite il portale del cliente
Per eseguire il provisioning di un'istanza del server virtuale temporanea tramite {{site.data.keyword.slportal}}, completa le seguenti istruzioni:

  1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} utilizzando le tue credenziali univoche.
  2. Individua la sezione **Order** e fai clic su **Devices**.
  3. In *Public Virtual Server* nella pagina *Devices*, fai clic su **Transient** per l'offerta Virtual Server.
  4. Nella pagina *Configure your Cloud Server*, compila tutte le informazioni pertinenti.
  5. Fai clic su **Add to Order** per continuare.
  6. Conferma o modifica le informazioni sul dominio per il server.
  7. Fai clic sulle caselle di spunta **Cloud Service terms** e **Third-Party Service Agreement**.
  8. Conferma o immetti le tue informazioni di pagamento e fai clic su **Submit Order**. Vieni reindirizzato a una schermata con il tuo numero di ordine di provisioning. Puoi stampare la schermata perché è anche la tua ricevuta dell'ordine di provisioning.

Puoi anche eseguire il provisioning di un server virtuale temporaneo utilizzando {{site.data.keyword.slapi_short}}. Per un esempio, consulta [Provisioning di un'istanza temporanea utilizzando Crea oggetto](/docs/vsi?topic=virtual-servers-api-rest-public#api-rest-transient).
{:tip}

## Passi successivi
Viene inviata una serie di email al tuo amministratore di riconoscimento dell'ordine di provisioning, l'approvazione e l'elaborazione e il completamento del provisioning. L'email di completamento del provisioning include un link alla pagina *Device Details*.
 
Dopo aver eseguito il provisioning del tuo server virtuale ed è possibile utilizzarlo, puoi configurare i tuoi server virtuali utilizzando la console
{{site.data.keyword.cloud_notm}} o la {{site.data.keyword.slapi_short}}. Per ulteriori informazioni, vedi [Configurazione di server virtuali](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).
