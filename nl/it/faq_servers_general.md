---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# FAQ: Server (generale)
{: #faqs-servers-general-}

## Qual è la differenza tra "Avvio da immagine" e "Carica da immagine"?
{:faq}

Sia Avvio da immagine che Carica da immagine utilizzano i template dell'immagine esistenti, che vengono applicati a un dispositivo per sostituire il sistema operativo esistente o per integrare il sistema operativo per tentare di risolvere un problema esistente. La differenza principale tra il processo di avvio e di caricamento è il tipo di immagine che viene utilizzato. Quando si eseguono i processi di avvio e caricamento dall'immagine, assicurati di aver eseguito il backup di tutti i dati che desideri ripristinare.

   * Avvio da immagine è un modo di avviare un dispositivo utilizzando una ISO fornita da {{site.data.keyword.BluSoftlayer_full}} per il ripristino del sistema o una ISO che è stata caricata utilizzando la funzione *Importa immagine* nella console {{site.data.keyword.cloud_notm}}. La ISO potrebbe essere una versione pulita del sistema operativo del dispositivo o un disco di ripristino che può essere utilizzato per tentare di correggere un problema con il dispositivo.
   * Carica da immagine è un metodo di ricaricamento del sistema operativo che utilizza un template dell'immagine che è stato acquisito da un dispositivo o caricato utilizzando la funzione *Importa immagine* nella console {{site.data.keyword.cloud_notm}}. L'opzione *Carica da immagine* esegue il ricaricamento utilizzando un VHD, che pulisce il dispositivo da tutti i dati e sostituisce i file e il sistema operativo esistenti con una versione "come nuova" dell'immagine selezionata.

## Perché non posso collegarmi alla console KVM?
{:faq}

Se non puoi collegarti alla console KVM, controlla i seguenti suggerimenti sulla risoluzione dei problemi come supporto per la risoluzione del problema. Se si verificano ulteriori problemi, contatta il supporto. Per ulteriori informazioni su come contattare il supporto, vedi [Come ottenere aiuto e supporto](/docs/vsi?topic=virtual-servers-gettinghelp#gettinghelp).

   * La console KVM è un applet Java. Java deve essere installato prima di accedere alla console. Per ulteriori informazioni sull'installazione di Java, consulta [Scaricare Java gratuitamente ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.java.com/en/download/){: new_window}.  
   * Se Java è installato, accertarti che la connessione sia stata stabilita utilizzando la VPN. Se non è stata stabilita una connessione, viene visualizzata un'avvertenza durante il tentativo di collegamento alla console KVM in cui viene richiesta una connessione VPN.
   * La console KVM può generare una o più finestre a comparsa durante il processo di connessione. Abilita le finestre a comparsa dalla console {{site.data.keyword.cloud_notm}} per garantire di poter stabilire una connessione.
   * Potresti ricevere un errore "Le applicazioni Java sono bloccate dalle tue impostazioni di sicurezza." Per i dispositivi iKVM bare-metal, devi aggiungere un'eccezione per l'indirizzo IP del dispositivo IPMI. Per i dispositivi VSI, accertarti di consentire "https://control.softlayer.com" e l'indirizzo IP del KVM. Per ulteriori informazioni, consulta [Perché le applicazioni Java sono bloccate dalle tue impostazioni di sicurezza con l'ultimo Java? ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}.
   * Se sono state rispettate le seguenti condizioni e ricevi un messaggio di errore che afferma, "Manca il manifest delle autorizzazioni richiesto in main.jar", le applet Java non sono state abilitate nel pannello di controllo Java. Queste impostazioni sono state introdotte come una precauzione di sicurezza da Oracle in Java SE v7. Abilita le applet nel pannello di controllo per risolvere questo problema.

     Se stai utilizzando Mac OSX insieme a Google Chrome, fai riferimento a Informazioni e requisiti del sistema per l'installazione e l'utilizzo di Mac Java 7 nel sito web Java.
     {:note}

   * Se si sta tentando di collegarsi a una VSI tramite Java standard e si stanno ricevendo soltanto errori, puoi anche tentare di utilizzare di utilizzare VNC.

Se hai completato tutti i precedenti controlli e ancora non riesci a collegarti alla console KVM, contatta il supporto per ulteriore assistenza per la risoluzione del problema. Se è stato eseguito un collegamento alla console ma si verificano dei problemi durante la connessione al dispositivo, assicurati che le credenziali che stanno venendo utilizzate per accedere siano valide. Contatta l'amministratore dell'account per verificare le credenziali, se necessario.

## Ho perso la mia password del server. Come posso recuperarla?
{:faq}

Se la password amministratore o root al tuo server ha smesso di funzionare all'improvviso, controlla i seguenti elementi. Se necessario, utilizza le istruzioni per avviare un kernel di salvataggio e reimposta la tua password.

   * Stai copiando e incollando la password? Se no, prova. Incolla inoltre la password nel blocco note per assicurarti che non vengano accidentalmente copiati degli spazi con la password.
   * Se il server ha il cPanel, è possibile che cPHulk abbia bloccato il tuo indirizzo IP a causa di tentativi di accesso non riusciti? In questo caso, puoi accedere al server utilizzando KVM o IPMI e aggiungere il tuo indirizzo IP in cPHulk con "/scripts/cphulkdwhitelist" seguito dal tuo indirizzo IP.
   * Qualcuno ha tentato recentemente di modificare la password per il server modificandola nella console {{site.data.keyword.cloud_notm}}? La modifica della password nella console {{site.data.keyword.cloud_notm}} modifica solo ciò che vedi come password. Non modifica la password che sta utilizzando il server. Se si verifica questo, puoi contattare il supporto, i quali normalmente possono ripristinare la password funzionante originale.
   * Potrebbe essere necessario avviare la modalità di salvataggio del tuo sistema operativo per poter ripristinare la tua password. Per ulteriori informazioni, consulta [Avvio di un kernel di salvataggio](/docs/vsi?topic=virtual-servers-launching-rescue#launching-rescue).

Se hai già tentato tutto questo e non sei ancora in grado di collegarti al server utilizzando la password, contatta il supporto utilizzando un ticket e richiede una reimpostazione della password. Il supporto dovrà riavviare il server per poter reimpostare la password, per cui assicurati di essere pronto ad approvare il riavvio e/o a fornire un intervallo di tempo di manutenzione in cui può essere eseguito. Molte reimpostazioni della password possono essere realizzate in 15 minuti. Nella console {{site.data.keyword.cloud_notm}}, puoi creare un ticket andando in **Supporto > Crea un caso** e utilizzare l'oggetto *Accounts & access*.

## Le partizioni LVM sono supportate come file system valido?
{:faq}

LVM (Logical Volume Management) fornisce la gestione logica dei file system in Linux. Nell'ambiente {{site.data.keyword.BluSoftlayer}}, LVM non è supportato come uno schema di partizionamento avviabile. Le istanze del server virtuale non possono essere ordinate con LVM e non è possibile eseguire il provisioning dell'importazione delle immagini che utilizzano LVM come partizione di riavvio. Se hai bisogno di LVM nella partizione di riavvio, l'offerta bare metal può supportare LVM al riavvio per alcuni sistemi operativi. Con la configurazione e il supporto SO appropriati, i dischi VSI secondari possono essere utilizzati per le partizioni LVM; tuttavia, è importante tenere presente che LVM non è un file system supportato per l'immagine flex e i template dell'immagine. Se hai ulteriori domande, apri un ticket con il team di supporto che può assisterti.

## Rotte 161.26.0.0/16 preconfigurate sugli host del cliente
{:faq}

{{site.data.keyword.BluSoftlayer_notm}} abilita una nuova rotta su tutti i nuovi server con provisioning per supportare prodotti futuri.
   * La rotta fa puntare un qualsiasi indirizzo nell'intervallo 161.26.0.0/16 (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) alla rete privata di backend.
   * Questo blocco di IP viene assegnato a {{site.data.keyword.BluSoftlayer_notm}} da IANA e non sarà pubblicizzato sull'Internet pubblico.
   * Soltanto i sistemi {{site.data.keyword.BluSoftlayer_notm}} saranno trattati al di fuori di questo spazio.
   * Le ACL sui server personalizzati, i server virtuali e i gateway Vyatta dovranno essere aggiornate per consentire agli host del cliente di utilizzare i servizi dell'infrastruttura configurati con gli indirizzi IP al di fuori di questo intervallo.

## Come aggiungere il nuovo instradamento per vari SO
{:faq}

   <table>
   <CAPTION>Tabella 1. Aggiunta di una rotta da SO</CAPTION>
   <THEAD>
   <TR>
   <th>Sistema operativo</th>
   <th>Passi</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard e Enterprise</td>
   <td>
   Aggiungi la rotta persistente dalla riga di comando immettendo:
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>Nota:</b> sostituisci 10.0.0.1 con il tuo indirizzo IP del gateway privato.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   Aggiungi la rotta persistente dalla riga di comando immettendo:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Nota:</b> sostituisci 10.0.0.1 con il tuo indirizzo IP del gateway privato.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web, Standard, Enterprise e Datacenter</td>
   <td>
   Aggiungi la rotta persistente dalla riga di comando immettendo:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Nota:</b> sostituisci 10.0.0.1 con il tuo indirizzo IP del gateway privato.
   </td>
   </tr>
    <tr>
   <td>RedHat, Fedora e CentOS</td>
   <td>
   Crea una nuova rotta modificando/creando il seguente file: <i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>Dopo aver creato questo file, devi aggiungere le seguenti informazioni in esso: <i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>Nota:</b> sostituisci 10.0.0.1 con il tuo indirizzo IP del gateway privato.
   </td>
   </tr>
   <tr>
   <td>Ubuntu e Debian</td>
   <td>
   Nel tuo file <i>/etc/network/interfaces</i>, aggiungi la seguente riga alla fine del file:
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>Nota:</b> sostituisci 10.0.0.1 con il tuo indirizzo IP del gateway privato.
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>Nota:</b> sostituisci 172.16.0.26 con il gateway della sottorete su cui è la macchina, che dovrebbe essere la stessa del gateway definito per la rotta 10.0.0./8.</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>Utilizza il seguente comando per aggiungere la rotta all'host ESXi:
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>Nota:</b> sostituisci 10.0.0.1 con il tuo indirizzo IP del gateway privato.</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>Crea un file della rotta statico in /etc/systemd/network denominato 10-static.network simile a:
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>Nota:</b> sostituisci 10.0.0.1 con il tuo indirizzo IP del gateway privato.</td>
   </tr>
   </TBODY>
   </table>

   <a name="top"></a>

## Nel caso di un problema con il sistema di monitoraggio posso effettuare un riavvio automatico E avvertire un tecnico del supporto nell'evento che il server ha smesso di rispondere?
{:faq}

Sì, con l'ordine del nostro servizio **Automated Reboot from Monitoring Failure**, puoi configurare il monitoraggio del sistema per riavviare automaticamente il server ed emettere un ticket per un tecnico del supporto se viene emesso un avviso di monitoraggio. Come servizio aggiuntivo, forniamo **NOC Monitoring**, in cui riceverai una notifica personale nel caso si verifichi un problema di monitoraggio. Per ulteriori informazioni su queste offerte, fai riferimento a [Monitoraggio server ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud/infrastructure/monitoring?cm_mc_uid=46846454197915580355142&cm_mc_sid_50200000=71138741559658182022){:new_window}.

## Cosa è un mirror cvsup?
{:faq}

Puoi eseguire l'aggiornamento in base a un mirror cvsup locale che era stato eseguito per tuo conto. Assicurati che il tuo supfile abbia la seguente voce:

```
*default host=cvsup.service.softlayer.com
```
{:pre }

Viene inoltre eseguito il mirror dei distfiles che sono disponibili da freebsd.org. Puoi aggiungere la seguente riga nel tuo file */etc/make.conf* per tentare di eseguire prima il download dal repository locale:

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

Se il file non viene trovato nell'ubicazione prevista, seguirà il singolo Makefile della porta e passerà al mirror successivo.
