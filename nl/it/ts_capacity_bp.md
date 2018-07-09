---



copyright:
  years: 2017
lastupdated: "2018-01-03"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Considerazioni sulla capacità

## Cosa sta succedendo

Quando esegui il provisioning di un server virtuale, potresti ricevere il seguente messaggio di errore: 

```
Non c'è capacità sufficiente per completare la richiesta.
```
{:screen}

Quando il provisioning non riesce, tutte le istanze del server virtuale in questa richiesta particolare non riescono.
{:tip}

## Perché sta succedendo

Un errore di capacità si verifica quando non ci sono risorse disponibili sufficienti nel router o nel data center per soddisfare la richiesta del servizio. Ci sono molti motivi per cui potresti ricevere questo errore. La disponibilità delle risorse cambia frequentemente, per cui puoi attendere e riprovare più tardi.

## Come risolverlo 

Puoi tentare di nuovo il provisioning utilizzando le seguenti strategie:

1. Esegui il provisioning specificando un router differente.  
2. Esegui il provisioning senza specificare un router.
3. Esegui il provisioning in un data center differente.
4. Esegui il provisioning di meno istanze. 
5. Estendi le istanze eseguendo il provisioning in più data center.
6. Esegui il provisioning di istanze di dimensioni più piccole.
7. Modifica la memoria VSI da SAN a LOCAL o da LOCAL a SAN. 



