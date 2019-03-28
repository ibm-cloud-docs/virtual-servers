---

copyright:
  years: 2014, 2017
lastupdated: "2017-12-12"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:screen: .screen}
{:tip .tip}
{:table: .aria-labeledby="caption"}

# Fazendo upgrade da velocidade da porta no Linux
{: #upgrading-port-speed-in-linux}

As velocidades de porta padrão para servidores clientes (para as redes públicas e privadas) é 10 Mbps. Se você quiser fazer upgrade de uma de suas velocidades de porta para 100 Mbps ou 1000 Mbps, abra um chamado com o nosso departamento de Vendas. As vendas solicitarão a aprovação dos encargos mensais e um técnico mudará os limites de velocidade da porta na rede.

Esses comandos afetam a conectividade do servidor. Sempre gerencie as conexões de rede conectando-se primeiramente ao IP no qual NÃO está trabalhando.
{:tip}

É possível verificar a velocidade atual de sua conexão executando os comandos a seguir:

    ```
    # ethtool eth#   (eth1 for public, eth0 for private)
    ```
    {: pre}

A saída exibirá as configurações atuais para essa conexão:

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

Configurações para eth1:

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

Para mudar a velocidade, edite o arquivo a seguir usando seu editor de texto favorito:

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)

Você localizará a linha a seguir:

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

Isso permite que a negociação automática, a velocidade e o duplex sejam forçados na inicialização, mantendo uma configuração consistente através de uma reinicialização.
A velocidade pode ser modificada para corresponder à sua nova velocidade da porta. Isso requer uma reinicialização da rede antes do uso da nova velocidade.

Todas as conexões forçadas a 1000 Mbps devem ter a negociação automática ativada no arquivo ifcfg-eth#.
{: tip}
