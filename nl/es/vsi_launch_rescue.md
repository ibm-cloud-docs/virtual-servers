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


# Inicio de un kernel de rescate 
{: #launching-rescue}

Rescue Kernel es un entorno de rescate diseñado para ofrecer a los clientes la posibilidad de colocar en línea un servidor nativo o un servidor virtual para solucionar problemas del sistema que normalmente solo se solucionarían mediante una recarga del SO. Rescue Kernel se debe iniciar en el {{site.data.keyword.slportal_full}}. Siga estos pasos para iniciar Rescue Kernel para un dispositivo.
{:shortdesc}

## Inicie un Rescue Kernel

1. Acceda al [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/) utilizando sus credenciales exclusivas.
2. En la lista de dispositivos, pulse el nombre del dispositivo que desea rescatar.
3. Pulse la lista desplegable *Acciones* en la esquina superior derecha y seleccione **Rescate**.
4. Pulse el botón **Sí** para transmitir el dispositivo a Rescue Kernel inmediatamente. Pulse el botón **No** si desea cancelar la acción.

## Siguientes pasos
Después de iniciar Rescue Kernel, el dispositivo se apaga y se rearranca en el kernel de rescate correspondiente al sistema operativo del dispositivo. Este proceso puede tardar varios minutos.

Puede acceder al dispositivo de forma remota desde la dirección IP del dispositivo. Puede acceder al dispositivo en Rescue Kernel utilizando las credenciales de root o admin para los dispositivos registrados en el {{site.data.keyword.slportal}}. Si utiliza Rescue Kernel, puede resolver y descubrir problemas igual que lo haría en un dispositivo arrancado de manera normal. Si es necesario, puede montar unidades en SO de Rescue Kernel. Para salir de Rescue Kernel y devolver el dispositivo a su entorno ordinario, rearranque el dispositivo en el {{site.data.keyword.slportal}} o rearranque desde el SO de Rescue Kernel.

Para obtener más información sobre el rearranque de un dispositivo, consulte [Gestión de servidores virtuales](../vsi/vsi_managing.html).

