---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Asignación de direcciones IP de servidor
{: #assigning-server-ip-addresses}

{{site.data.keyword.cloud}} configura las instancias de servidor virtual con una dirección IPv4 en la red privada y, si se solicita, con una dirección IPv4 pública (de cara a internet). Además, puede solicitar una dirección IPv6 en la red pública. Todas estas direcciones IP reciben en conjunto el nombre de _direcciones IP primarias_.
{:shortdesc}

Se pueden vincular direcciones IP adicionales a las instancias de servidor virtual tras adquirir subredes secundarias a través de la consola de {{site.data.keyword.cloud_notm}}. Si adquiere direcciones IP de este modo y las gestiona, reciben el nombre de _direcciones IP secundarias_.

Para obtener más información sobre las opciones disponibles para adquirir direcciones IP, consulte [Subredes de IP](/docs/infrastructure/subnets?topic=subnets-about-subnets-and-ips).

## Vinculación de direcciones IP secundarias

Después de adquirir y direccionar una subred secundaria, debe configurar el sistema operativo de modo que utilice una o varias de las nuevas direcciones IP disponibles. Los pasos de configuración de las nuevas direcciones IP son distintos para cada sistema operativo, pero esta configuración suele recibir el nombre de configuración de "alias de interfaz". Consulte la documentación de su sistema operativo para obtener más detalles de configuración.
