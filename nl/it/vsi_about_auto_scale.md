---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords: auto scale, virtual servers

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Informazioni sul ridimensionamento automatico
{: #about-auto-scale}

Il ridimensionamento automatico per le istanze del server virtuale di {{site.data.keyword.cloud}} ti fornisce la capacità di automatizzare il processo di ridimensionamento manuale associato all'aggiunta o alla rimozione delle istanze per supportate le tue applicazioni di business. Questo ti consente di configurare automaticamente delle nuove istanze quando sono necessarie e tali istanze vengono arrestate e rimosse quando diminuisce il carico extra. Il ridimensionamento automatico utilizza i gruppi per contenere le politiche che modificano il modo in cui il tuo ambiente si espande o si restringe. Queste politiche utilizzano le azioni per aggiungere o rimuovere server virtuali in base alle tue esigenze di business e applicative.
{:shortdesc}

Il ridimensionamento automatico abilita le seguenti funzioni: 

* Ridimensionamento incrementale automatico e continuo delle istanze quando sono necessarie più risorse a causa della domanda
* Ridimensionamento decrementale automatico e continuo delle istanze rimuovendo le risorse non necessarie quando la domanda scende (risparmi denaro)
* Trigger di ridimensionamento flessibili: la percentuale di CPU, la larghezza di banda privata e pubblica in uscita e in entrata
* Aggiornamenti di stato quasi in tempo reale per l'attività di ridimensionamento nei gruppi
* Integrazione facoltativa della LAN virtuale (VLAN) e dei programmi di bilanciamento del carico locali

Ci sono due soluzioni di business comuni a cui può essere applicato il ridimensionamento automatico: 

|Soluzione| Descrizione |
| -------- | ----------- |
| [Ridimensionamento basato sulle pianificazioni](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling) | Il ridimensionamento basato sulle pianificazioni può essere utilizzato per configurare delle politiche per i picchi di utilizzo basati sul tempo, come ad esempio durante i fine settimana o durante le festività. Il ridimensionamento basato sulle pianificazioni può essere utilizzato quando una società si aspetta un picco nel traffico, ad esempio un sito di social networking richiede ulteriori risorse in base a una pianificazione. |
| [Ridimensionamento basato sulle risorse](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling) | Il ridimensionamento basato sulle risorse può essere utilizzato per configurare delle politiche per picchi irregolari, sulla base dell'utilizzo delle risorse.  Picchi irregolari nel traffico possono verificarsi quando viene fatto uno sforzo per introdurre un prodotto sul mercato oppure un sito di e-commerce sta proponendo una svendita e sono necessarie delle risorse per sostenere i tempi di risposta. |
{: caption="Tabella 1. Soluzioni di ridimensionamento automatico " caption-side="top"}

Se non sei l'amministratore dell'account, il tuo account utente deve includere l'autorizzazione per utilizzare il ridimensionamento automatico. L'amministratore dell'account può concedere l'autorizzazione dell'utente dalla console {{site.data.keyword.cloud_notm}}. Per ulteriori informazioni sull'aggiornamento delle autorizzazioni, consulta [Configurazione delle autorizzazioni dell'utente per il ridimensionamento automatico](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
{:note}


