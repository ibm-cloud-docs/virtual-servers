---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Downgrade delle velocità della porta
{: #downgrading-port-speeds}

Puoi temporaneamente diminuire le velocità della porta per la tua istanza del server virtuale senza aprire un ticket. Puoi solo diminuire, disconnettere o riconnettere al massimo di quello per cui stai già pagando. Non puoi eseguire l'upgrade da questa opzione. Le modifiche rimangono nella console finché non le annulli. Non viene effettuata alcuna modifica alla fatturazione per questo e il downgrade temporaneo del server non diminuisce la tua fattura. Se hai bisogno di una modifica permanente alla velocità della tua porta, devi aprire un ticket di vendita.
{:shortdesc}

## Informazioni preliminari
Per prima cosa passa al menu del dispositivo e assicurati di disporre delle autorizzazioni account corrette per completare l'attività.  

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/vsi?topic=virtual-servers-navigating-devices).
* Assicurati di avere tutte le autorizzazioni account necessarie e l'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione dell'infrastruttura classica **Manage Users**, può modificare le autorizzazioni. 

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione accesso dispositivo](/docs/vsi?topic=virtual-servers-managing-device-access).

## Downgrade delle velocità della porta
Completa la seguente procedura per diminuire le velocità della porta.

1. Dal menu **Devices**, seleziona **Device List**.
2. Seleziona il server che vuoi aggiornare.
3. Nella scheda **Overview**, vai a **Network details**.
4. Seleziona il menu a discesa **Speed** (sia per la rete privata che pubblica) per diminuire o scollegare la velocità della porta.

Quando modifichi le velocità della porta o le disconnetti per un qualsiasi motivo, devi modificare manualmente il server stesso.
{:tip}
