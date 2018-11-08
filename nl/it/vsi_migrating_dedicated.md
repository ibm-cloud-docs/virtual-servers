---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Migrazione di un'istanza host dedicata a un altro host
{: #migrating-dedicated-host}

Puoi migrare le tue istanze host dedicate da un host a un altro nello stesso POD. Seleziona l'istanza da migrare dalla pagina dei dettagli del dispositivo dell'host o dell'istanza. Tieni presente che possono venire migrate solo due istanze alla volta e il tempo necessario per la migrazione dipende dal disco. I dischi SAN vengono migrati più velocemente perché i dischi locali richiedono la copia del disco. Le istanze di migrazione sono offline durante la migrazione; l'host rimane attivo per qualsiasi altra istanza host dedicata.
{:shortdesc}

Utilizza le seguenti istruzioni per migrare le istanze host dedicate a un altro host dedicato nello stesso POD dalla pagina dei dettagli del dispositivo dell'*host dedicato originale*. 

1. Accedi al [{{site.data.keyword.slportal_full}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) utilizzando le tue credenziali univoche. 
2. Fai clic su **Device > Device List** e seleziona l'host e l'istanza host dall'elenco.
3. Fai clic sull'elenco a discesa **Actions** accanto all'istanza dedicata da migrare.
4. Seleziona **Migrate** e immetti l'host in cui viene migrata l'istanza; ricorda, l'host di destinazione deve essere nello stesso POD dell'host originale.
5. Fai clic sul pulsante **Migrate**. 

La migrazione inizierà immediatamente. Durante la migrazione, l'istanza dedicata è offline finché non migrata al proprio nuovo host. Puoi visualizzare la pagina dei dettagli del dispositivo dell'host di destinazione per assicurarti che l'istanza sia stata migrata correttamente.

Utilizza le seguenti istruzioni per migrare le istanze host dedicate a un altro host dedicato nello stesso POD dalla pagina dei dettagli dell'*istanza host dedicata*.

1. Accedi al [{{site.data.keyword.slportal}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/) utilizzando le tue credenziali univoche.
2. Fai clic su **Device > Device List** e seleziona l'istanza ospitata da migrare dall'elenco.
3. Fai clic sul link **Migrate** nel lato destro della pagina.
4. Seleziona l'host di destinazione a cui migrare l'istanza; ricorda, l'host di destinazione deve essere nello stesso POD dell'host originale.
5. Fai clic sul pulsante **Migrate**.

La migrazione inizierà immediatamente. Durante la migrazione, l'istanza dedicata è offline finché non migrata al proprio nuovo host. Puoi visualizzare la pagina dei dettagli del dispositivo dell'host di destinazione per assicurarti che l'istanza sia stata migrata correttamente.

## Passi successivi
Dopo aver migrato un'istanza host dedicata, controlla che la migrazione abbia funzionato verificando se il suo stato è verde nella pagina dei dettagli del dispositivo del nuovo host dedicato.
