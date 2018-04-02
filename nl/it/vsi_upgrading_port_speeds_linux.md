---



copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:screen: .screen}
{:tip .tip}
{:table: .aria-labeledby="caption"}

# Upgrade della velocità della porta in Linux

Le velocità della porta predefinite per i server del cliente (sia per le reti private che pubbliche) sono 10 Mbps. Se vuoi aggiornare una delle tue velocità della porta a 100 Mbps o 1000 Mbps, apri un ticket con il nostro dipartimento delle vendite. Il dipartimento delle vendite ti chiederà di approvare l'addebito mensile e un tecnico modificherà i limiti di velocità della porta nella rete.

Questi comandi influenzano la connettività del tuo server. Gestisci sempre le connessioni di rete collegandoti prima all'IP con cui NON stai lavorando.
{:tip}

Puoi controllare la velocità corrente della tua connessione immettendo i seguenti comandi:

    ```
    # ethtool eth#   (eth1 for public, eth0 for private)
    ```
    {: pre}

L'output visualizzerà le configurazioni correnti per tale connessione:

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

Impostazioni per eth1:

        Supported ports: [ MII ]
        Supported link modes:   10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Supports auto-negotiation: Yes
        Advertised link modes:  10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Advertised auto-negotiation: Yes
        Speed: 100Mb/s
        Duplex: Full
        Port: MII
        PHYAD: 3
        Transceiver: external
        Auto-negotiation: on
        Supports Wake-on: g
        Wake-on: d
        Link detected: yes
        root@noc-training-linux [~]#

Per modificare la velocità, modifica il seguente file utilizzando il tuo editor di testo preferito:

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)

Troverai la seguente riga:

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

Questo permette alla negoziazione automatica, alla velocità e al duplex di essere forzati all'avvio, mantenendo una configurazione coerente tramite un riavvio.
La velocità può essere modificata in modo che corrisponda alla tua nuova velocità della porta. Questo richiede un riavvio di rete prima che venga utilizzata la nuova velocità.

Tutte le connessioni forzate a 1000 Mbps devono avere autoneg abilitato nel file ifcfg-eth#.
{: tip}
