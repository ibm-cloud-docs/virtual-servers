---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-10"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Hosts dedicados e instancias dedicadas 

Los hosts dedicados son servidores virtuales que le permiten especificar el centro de datos y POD donde desea colocar el host. Puede asignar instancias o máquinas virtuales a un host específico para maximizar el control de la colocación de la carga de trabajo y para opciones flexibles de costes de suministro.
{:shortdesc}

## Capacidad garantizada
Tiene garantizada la capacidad dentro del centro de datos y POD donde esté colocado el host. Por ejemplo, si el POD que contiene el host dedicado y las instancias dedicadas alcanza su capacidad, puede seguir asignando instancias dedicadas al host si este dispone del espacio adecuado.

## Cargas de trabajo visibles
Puede ver el consumo general de recursos correspondiente a todas las instancias dedicadas asignadas a un host dedicado en una página. Ver el uso de núcleo, RAM y almacenamiento local le ayuda a determinar si tiene que migrar instancias dedicadas a otro host dedicado. Este nivel de granularidad le ofrece la capacidad necesaria para gestionar las cargas de trabajo con el máximo control. 

## Gestión posterior al despliegue
Además de la capacidad garantizada y la visibilidad de sus cargas de trabajo, puede migrar sus instancias dedicadas entre hosts dedicados para maximizar el control sobre la colocación de la carga de trabajo.

## Mantenimiento
Ocasionalmente, el mantenimiento de la infraestructura requiere un host dedicado para reiniciarse. Por ejemplo, es posible que el hipervisor Xen necesite una actualización. Si tiene varios hosts dedicados, tiene las opciones siguientes para minimizar el tiempo de inactividad de mantenimiento. 
* El mantenimiento lo realizan los POD dentro de un centro de datos. Puede desplegar los hosts dedicados para separar los POD para distribuir el mantenimiento necesario. 
* Puede crear una incidencia de soporte para un host dedicado para solicitar que se retrasen un mantenimiento planificado. Durante este tiempo, puede migrar instancias dedicadas (fuera de línea) entre hosts dedicados en el mismo POD.

## Alta disponibilidad
Si falla un host dedicado, las cargas de trabajo del host dedicado se migran automáticamente a un nuevo host dedicado. Las instancias dedicadas permanecen dedicadas a lo largo del ciclo de vida del servidor virtual.

En escenarios de alta disponibilidad, es posible que desee tener designado un host dedicado adicional. Por ejemplo, el host dedicado adicional le proporciona la flexibilidad para migrar las cargas de trabajo para las ventanas de mantenimiento.
