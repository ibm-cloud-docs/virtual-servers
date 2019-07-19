---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-06"

subcollection: virtual-servers

---

{:note: .note}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Opciones de almacenamiento
{: #storage-options}

Puede elegir el almacenamiento SAN (SAN portátil) o local para cada servidor virtual. Puede complementar SAN o el almacenamiento local con otros productos de almacenamiento, si es necesario.

## Almacenamiento local

El almacenamiento local se basa en discos que son locales para el host del servidor virtual. El almacenamiento local proporciona un mejor rendimiento de lectura/escritura de disco. Los discos se basan en una configuración de matriz redundante de discos independientes (RAID) que ofrece funciones de redundancia, sustitución de disco y supervisión de estado, que gestiona {{site.data.keyword.cloud}}. En los centros de datos más recientes, este almacenamiento es una unidad de estado sólido (SSD) para proporcionar el mejor rendimiento.

## Almacenamiento SAN portátil

Los volúmenes de almacenamiento portátil son soluciones de almacenamiento auxiliares que están disponibles exclusivamente en {{site.data.keyword.BluVirtServers_short}}.  El almacenamiento SAN portátil está basado en todos los clústeres de almacenamiento flash de {{site.data.keyword.cloud_notm}} en lugar de en el almacenamiento de host local. Esta infraestructura proporciona una mayor capacidad de recuperación en el caso de que se produzca un error en el host y también admite volúmenes mucho mayores. Si se produce un error del host, las instancias del servidor virtual que utilizan almacenamiento basado en SAN se migran automáticamente a otros hosts y se reinician.

El almacenamiento portátil es una solución ideal si desea transferir datos entre servidores virtuales que existen en cualquier centro de datos de la red de {{site.data.keyword.cloud_notm}}. Los volúmenes de almacenamiento portátil son útiles para aplicaciones de base de datos que requieren acceso a almacenamiento de nivel de bloque en bruto no formateado y para mover conjuntos de datos grandes entre {{site.data.keyword.BluVirtServers_short}}.

Todos los discos secundarios están conectados como almacenamiento portátil. En la mayoría de los casos, estos discos secundarios se pueden desconectar en cualquier momento para permitirles que se trasladen a otros servidores virtuales.

Con los servidores virtuales públicos que utilizan el almacenamiento local equilibrado, no se pueden desconectar los discos primarios ni secundarios.
{:important}

Los discos se pueden volver a conectar a otro servidor, siempre que el cambio no supere la cuota de disco o el límite de tamaño de volumen máximo del servidor virtual de destino.

El disco trasladado pasa a ser el tipo de almacenamiento del servidor de destino.
{:note}

Cuando un volumen de almacenamiento portátil está conectado a un servidor virtual en un centro de datos distinto del servidor virtual original, el sistema interno de {{site.data.keyword.cloud_notm}} copia el volumen al SAN en el nuevo centro de datos. El sistema verificará entonces la integridad del volumen copiado y elimina el volumen portátil original desde el SAN del centro de datos original.

## Limitaciones de LVM

La gestión de volúmenes lógicos (LVM) no recibe soporte como esquema de particionamiento arrancable. Con la configuración y el soporte de sistema operativo adecuados, los discos del servidor virtual secundario se pueden utilizar para particiones LVM. Sin embargo, LVM no es un sistema de archivos soportado para plantillas de imágenes o imágenes flex.

## Almacenamiento suplementario

Los servidores virtuales son totalmente compatibles con {{site.data.keyword.filestorage_short}} y {{site.data.keyword.blockstorageshort}}, así como con {{site.data.keyword.cos_full}}. Estos tipos de almacenamiento son los recomendados para unidades de clúster, almacenamiento de archivos compartidos, almacenamiento de archivado, grandes requisitos de almacenamiento o requisitos de rendimiento específicos.

Para obtener más información sobre las opciones de almacenamiento adicionales, consulte los recursos siguientes:

* [Iniciación a Almacenamiento en bloque](/docs/infrastructure/BlockStorage?topic=BlockStorage-getting-started)
* [Iniciación a Almacenamiento de archivos](/docs/infrastructure/FileStorage?topic=FileStorage-getting-started)
* [Iniciación a Almacenamiento de objetos](/docs/services/cloud-object-storage?topic=cloud-object-storage-getting-started)

## Siguientes pasos
Para obtener más información sobre cómo utilizar los volúmenes de almacenamiento portátil, consulte las tareas siguientes:
* [Gestión del almacenamiento portátil](/docs/vsi?topic=virtual-servers-accessing-portable-storage#accessing-portable-storage)
* [Edición de una descripción de almacenamiento portátil](/docs/vsi?topic=virtual-servers-editing-a-portable-storage-description#editing-a-portable-storage-description)
