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

# Actualización de la velocidad de puerto en Linux
{: #upgrading-port-speed-in-linux}

La velocidad de puerto predeterminada para servidores de clientes (para redes públicas y privadas) es 10 Mbps. Si le gustaría actualizar las velocidades de puerto a 100 Mbps o 1000 Mbps, abra una incidencia con nuestro departamento de ventas. Ventas le solicitará que apruebe el cargo mensual y un técnico cambiará los límites de velocidad de puerto en la red.

Estos mandatos afectan a la conectividad de su servidor. Gestione siempre las conexiones de red conectándose primero a la IP en la que NO esté trabajando.
{:tip}

Puede comprobar la velocidad actual de la conexión ejecutando los mandatos siguientes:

    ```
    # ethtool eth#   (eth1 para pública, eth0 para privada)
    ```
    {: pre}

La salida mostrará las configuraciones actuales para esta conexión:

    ```
    root@noc-training-linux [~]# ethtool eth1
    ```
    {: screen}

Valores para eth1:

        Puertos soportados: [ MII ]
        Modos de enlace soportados:   10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Soporta la negociación automática: Sí
        Modos de enlace publicitado:  10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Negociación automática publicitada: Sí
        Velocidad: 100Mb/s
        Dúplex: Full
        Puerto: MII
        PHYAD: 3
        Transceptor: externo
        Negociación automática: activada
        Soporta Wake-on: g
        Wake-on: d
        Enlace detectado: sí
        root@noc-training-linux [~]#

Para cambiar la velocidad, edite el archivo siguiente utilizando su editor de texto preferido:

    /etc/sysconfig/network-scripts/ifcfg-eth#   (ifcfg-eth1 for public, ifcfg-eth0 for private)

Encontrará la línea siguiente:

    ETHTOOL_OPTS="autoneg off speed 100 duplex full"

Esto permite forzar la negociación automática, la velocidad y el dúplex al arrancar, manteniendo una configuración coherente mediante un rearranque.
La velocidad puede modificarse para que coincida con la nueva velocidad de puerto. Esto requiere rearrancar la red antes de utilizar la nueva velocidad.

Todas las conexiones forzadas a 1000 Mbps deben tener habilitada la negociación automática (autoneg) en el archivo ifcfg-eth#.
{: tip}
