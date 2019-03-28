---

copyright:
  years: 2017
lastupdated: "2017-10-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Server virtuali dedicati
{: #dedicated-virtual-servers}

L'offerta dell'host dedicato per l'infrastruttura {{site.data.keyword.Bluemix}} è un server dedicato, virtualizzato e a singolo tenant. Fornisce il massimo controllo sul posizionamento del carico di lavoro e opzioni di post provisioning flessibili. Puoi decidere in quale data center {{site.data.keyword.cloud}} predeterminato vengono collocati i tuoi server virtuali e può essere garantita la capacità assegnando gli host direttamente al tuo account.
{:shortdesc}

L'offerta include le seguenti funzioni:

* Affinità e anti-affinità. Puoi specificare le relazioni host-to-virtual server e virtual server-to-virtual server che devono rimanere, che sono conosciute come le regole di affinità e anti-affinità. Queste regole di aiutano ad assicurarti che i tuoi carichi di lavoro siano posizionati appropriatamente in base ai tuoi requisiti del carico di lavoro.
* Gestione post distribuzione. Puoi migrare i server virtuali tra gli host dedicati in base ai tuoi requisiti del carico di lavoro.
* Visibilità carico di lavoro. Puoi visualizzare il consumo delle risorse, ovvero core, RAM e archiviazione locale, per ciascun host, il che ti offre il massimo controllo sulla gestione del tuo carico di lavoro.

Puoi scegliere tra due modelli di distribuzione: host dedicati e istanze dedicate. Gli host dedicati aiutano nel controllo del posizionamento del carico di lavoro e le istanze dedicate offrono l'isolamento a singolo tenant.

**Nota:** le istanze dedicate non forniscono alcune delle funzioni di controllo offerte dagli host dedicati.  Consulta la seguente tabella per ulteriori dettagli.
<table>
<CAPTION>Tabella 1. Funzioni di controllo</CAPTION>
<THEAD>
<TR>
<th>Funzione server virtuale dedicato</th>
<th>Istanze host dedicate</th>
<th>Istanze dedicate</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>Isolamento a singolo tenant</td>
<td>X</td>
<td>X</td>
</tr>
<tr>
<td>Controllo posizionamento del server virtuale</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Visibilità della risorsa</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Fatturazione istanza</td>
<td></td>
<td>X</td>
</tr>
<tr>
<td>Fatturazione host<sup>(1)</sup></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Controllo post distribuzione</td>
<td>X</td>
<td></td>
</tr>
<tr>
<td>Riserve capacità</td>
<td>X</td>
<td></td>
</tr>
</TBODY>
</table>


<sup>(1)</sup>Il prezzo dell'host è comprensivo di core, RAM, SSD locale e velocità di rete. Il prezzo del sistema operativo Premium, l'archiviazione SAN (storage area network) e i componenti aggiuntivi software sarà stabilito per istanza in base al prezzo e alle licenze esistenti in un modello orario o mensile.

Tieni presente quanto segue quando ordini gli host dedicati e le istanze host dedicate:

* La posizione del tuo host; poi scegliere tra i seguenti data center {{site.data.keyword.cloud_notm}}:

| Data Center          ||
| ------------ | ------- |
|AMS01         |  MON01  |
|AMS03         |  OSL01  |
|CHE01         |  PAR01  |
|DAL05         |  SAO01  |
|DAL06         |  SEO01  |
|DAL09         |  SJC01  |
|DAL10         |  SJC03  |
|DAL12         |  SJC04  |
|DAL13         |  SNG01  |
|FRA02         |  SYD01  |
|HKG02         |  SYD04  |
|HOU02         |  TOK02  |
|LON02         |  TOR01  |
|LON04         |  WDC01  |
|MEL01         |  WDC04  |
|MEX01         |  WDC06  |
|MIL01         |  WDC07  |
{: caption="Tabella 2. Data center supportati" caption-side="top"}

* La dimensione dei tuoi host viene determinata dai tuoi carichi di lavoro che stai eseguendo su di essi. L'impostazione predefinita è 56 Core X 242 GB RAM X 1.2 TB.
* Puoi ordinare solo due host alla volta. Ad esempio, se hai bisogno di sei host, devi posizionare tre ordini separati.
* Ogni host avrà bisogno del proprio nome univoco e puoi assegnare automaticamente il tuo POD.

## Passi successivi

Dopo aver controllato e deciso le tue opzioni di distribuzione, è il momento di eseguire il provisioning del tuo server virtuale. Per iniziare, consulta [Provisioning delle istanze e degli host dedicati](/docs/vsi?topic=virtual-servers-ordering-vs-dedicated).
