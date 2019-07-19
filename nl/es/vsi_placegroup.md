---

copyright:
  years: 2018, 2019
lastupdated: "2019-04-24"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Grupos de colocación
{: #placement-groups}

La alta disponibilidad (HA) es un aspecto importante de cualquier despliegue en la nube. Ya sea el sitio web de su negocio de comercio electrónico o una base de datos de producción utilizada por la aplicación principal de su empresa, necesita que esté siempre activo. Con este fin, nuestros clientes de arquitectura de TI trabajan duro en construir una arquitectura resistente para tratar de obtener los porcentajes más altos posibles de tiempo de actividad. Aunque el tiempo de actividad se supervisa detalladamente dentro de las organizaciones de TI, puede caer por debajo de los niveles clave o experimentar cortes sustanciales, lo cual supone un enorme problema para toda la empresa.

La creación de redundancia en cada nivel de la infraestructura para eliminar cualquier punto único de anomalía (SPOF) es vital para tener un buen rendimiento en relación con esta métrica. Para las cargas de trabajo que se ejecutan en servidores virtuales, esto implica implementar soluciones de migración tras error con varios servidores virtuales que puedan sustituirse automáticamente entre sí en caso de que se produzca un bloqueo.

No obstante, a menos que se suministren los servidores virtuales públicos en distintos centros de datos, realmente no hay manera de determinar dónde se puede colocar cada uno de ellos en relación con los demás. Esto puede ser problemático si 1) construye con la alta disponibilidad como objetivo y 2) los servidores virtuales caen en el mismo host físico, dejándolos vulnerables a una parada en una única parte del hardware. Aunque puede que esto no sea probable, los gestores de TI no pueden permitir que exista la posibilidad de un SPOF en aplicaciones críticas. La construcción en centros de datos es una opción, pero esto puede introducir desafíos de la red que requieren dispositivos adicionales o que aumentan la latencia, especialmente en regiones con un único centro de datos.

El diseño de grupos de colocación para los servidores virtuales de {{site.data.keyword.cloud}} resuelve este problema. Los grupos de colocación le ofrecen una medida de control sobre el host en el que se coloca un nuevo servidor virtual público. Con este release, hay una regla de "dispersión", que implica que los servidores virtuales dentro de un grupo de colocación se dispersan todos en distintos hosts. Puede crear una aplicación de alta disponibilidad dentro de un centro de datos sabiendo que los servidores virtuales están aislados unos de otros.

La creación de grupos de colocación con la regla de "dispersión" está disponible en centros de datos de {{site.data.keyword.cloud_notm}} selectos. Una vez creado, puede suministrar un nuevo servidor virtual en dicho grupo y garantizar que no estará en el mismo host que ningún otro de los demás servidores virtuales. Y ahora viene lo mejor: No hay absolutamente ningún coste asociado al uso de esta característica. Si están disponibles, los grupos de colocación de {{site.data.keyword.cloud_notm}} para servidores virtuales son una característica gratuita.

Puede crear el grupo de colocación y luego asignar hasta cinco nuevas instancias de servidor virtual. Con la regla de "dispersión", se suministra cada uno de los servidores virtuales en hosts físicos diferentes.

## Siguientes pasos

Para crear y gestionar nuevos grupos de colocación, consulte [Gestión de grupos de colocación](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup#vsi_managing_placegroup).
