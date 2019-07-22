---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-22"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Prezzi host dedicati
{: #dedicated-virtual-server-pricing}

I prezzi per gli host dedicati vengono offerti in un modello mensile e orario.
{:shortdesc}

I prezzi degli host dedicati includono tutti i componenti vCPU, RAM, archiviazione locale e velocità della porta di uplink dopo il provisioning delle istanze negli host dedicati. Per ulteriori informazioni sui prezzi, consulta [Virtual servers provisioning calculator ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

Con gli host dedicati, sono disponibili dischi di archiviazione locale aggiuntivi sul primo, secondo, terzo, quarto e quinto disco. Viene inoltre fornita capacità aggiuntiva fino a 400 GB per ogni disco secondario.

Il provisioning delle istanze orarie può essere eseguito su host mensili e orari. Il provisioning delle istanze mensili può essere eseguito solo su host mensili.

| Configurazione host | vCPU	| RAM (GB) | Archiviazione locale (TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |  56 	|   242    |        	1.2	          |
| 56x484x1.2         |  56  |   484    |          1.2           |
{: caption="Tabella 1. Configurazioni host dedicato" caption-side="top"}

I prezzi variano per regione.
{:note}

SAN (rete collegata), SO premium e i componenti aggiuntivi SW sono addebitati in modo orario o mensile, dall'istanza, a seconda dell'istanza con provisioning sull'host dedicato. I prezzi per questi tre componenti sono coerenti con l'offerta esistente per le istanze pubbliche e dedicate. 

Ad esempio, un'istanza dedicata con provisioning su un host dedicato con la seguente configurazione non viene addebitata dall'istanza. vCPU, RAM, archiviazione locale e velocità della porta di uplink sono inclusi negli addebiti dell'host dedicato. 

* 8 vCPU
* 16 GB RAM
* 100 GB locali primo disco SSD
* 400 GB locali secondo disco SSD
* 400 GB locali terzo disco SSD
* 1 Gbps uplink rete privata e pubblica (host dedicato) 

