---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Acerca de los volúmenes de almacenamiento portátil

Los volúmenes de almacenamiento portátil son soluciones de almacenamiento auxiliares que están disponibles exclusivamente en {{site.data.keyword.BluVirtServers_short}}. Pueden estar conectados a un servidor virtual a la vez. También son una solución ideal si desea transferir datos entre servidores virtuales que existen en cualquier centro de datos de la red de {{site.data.keyword.cloud}}. Los volúmenes de almacenamiento portátil son útiles para aplicaciones de base de datos que requieren acceso a almacenamiento de nivel de bloque en bruto no formateado y para mover conjuntos de datos grandes entre {{site.data.keyword.BluVirtServers_short}}.

Cuando un volumen de almacenamiento portátil está conectado a un servidor virtual en un centro de datos distinto del servidor virtual original, el sistema interno de {{site.data.keyword.cloud}} copia el volumen al SAN en el nuevo centro de datos. El sistema verificará entonces la integridad del volumen copiado y elimina el volumen portátil original desde el SAN del centro de datos original.

## Siguientes pasos
Para obtener más información sobre cómo utilizar los volúmenes de almacenamiento portátil, consulte las tareas siguientes:
* [Acceso a almacenamiento portátil](/docs/vsi/storage?topic=virtual-servers-accessing-portable-storage)
* [Edición de la descripción de almacenamiento portátil](/docs/vsi/storage?topic=virtual-servers-editing-a-portable-storage-description)
