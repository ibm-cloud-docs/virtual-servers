---

copyright:
  years: 2018
lastupdated: "2018-08-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Assegnazione degli indirizzi IP del server
{: #assigning-server-ip-addresses}

{{site.data.keyword.cloud}} configura le istanze del server virtuale con un indirizzo IPv4 sulla rete privata e, se richiesto, un indirizzo IPv4 (verso internet) pubblico. Inoltre, puoi richiedere un indirizzo IPv6 sulla rete pubblica. Tutti questi indirizzi IP vengono considerati collettivamente come _Indirizzi IP primari_.
{:shortdesc}

Ulteriori indirizzi IP possono essere collegati alle istanze del server virtuale dopo l'acquisto di sottoreti secondarie tramite [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com). Gli indirizzi IP acquistati in questo modo e gestiti da te sono indicati come _Indirizzi IP Secondari_.

Per ulteriori informazioni sulle opzioni disponibili per l'acquisizione degli indirizzi IP, consulta [Sottoreti e IP](/docs/infrastructure/subnets?topic=subnets-getting-started-with-subnets-and-ips#getting-started-with-subnets-and-ips).

## Bind degli indirizzi IP secondari

Dopo aver acquistato e instradato una sottorete secondaria, devi configurare il sistema operativo per utilizzare uno o più degli indirizzi IP appena disponibili. La procedura di configurazione per i nuovi indirizzi IP è diversa per ogni sistema operativo, ma l'impostazione viene normalmente indicata come "alias dell'interfaccia". Consulta la documentazione del tuo sistema operativo per ulteriori dettagli sulla configurazione.
