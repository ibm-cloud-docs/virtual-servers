---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Firewall
{: #virtual-server-security-options}

Con {{site.data.keyword.BluVirtServers}}, disponi di diverse opzioni firewall che forniscono una livello di sicurezza essenziale.  Viene eseguito il provisioning delle opzioni firewall su richiesta, senza interruzioni del servizio. I servizi firewall impediscono al traffico non desiderato di raggiungere i tuoi server, riducendo il rischio di un attacco e consentendo alle tue risorse server di essere dedicate al loro utilizzo previsto.
{:shortdesc}

I firewall sono disponibili come una funzione aggiuntiva per tutti i server nella rete pubblica dell'infrastruttura.

Come parte del processo di ordine, puoi selezionare l'hardware specifico per il dispositivo o un firewall software per fornire protezione. In alternativa, puoi distribuire le applicazioni firewall dedicate all'ambiente e distribuire il server virtuale a una VLAN protetta.  

Un server virtuale non può essere protetto da due applicazioni firewall nella stessa interfaccia.
{:note}

Per ulteriori informazioni, consulta le seguenti raccolte di argomenti di sicurezza.

* [Firewall hardware (condivisi)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Firewall hardware (dedicati)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)
