---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Servidores virtuales transitorios
La oferta de {{site.data.keyword.BluVirtServers}} transitorios es una buena opción si tiene cargas de trabajo flexibles y quiere ahorrar en costes. Conseguirá ahorrar si ejecuta su carga de trabajo en un servidor virtual transitorio. Las instancias transitorias se suministran cuando hay capacidad no utilizada disponible. Por tanto, cuando se necesitan recursos del centro de datos para cuentas bajo demanda completas, también puede perder estos recursos. Las instancias transitorias dejan de suministrarse cuando estos recursos se reclaman.   

Los servidores virtuales transitorios ofrecen la siguiente flexibilidad:

* **Disponibilidad global** 

    La oferta de servidor virtual transitorio está disponible en los centros de datos de todo el mundo.
    
* **Ahorro en costes** 

    Los servidores virtuales transitorios son ideales para cargas de trabajo de no producción. Por ejemplo, podría utilizar una instancia transitoria para probar y desarrollar aplicaciones o para probar la escalabilidad en entornos que no requieran un tiempo de funcionamiento constante.

Las instancias transitorias son instancias públicas que utilizan almacenamiento respaldado por SAN.

## Notificaciones
Puede utilizar la {{site.data.keyword.slapi_short}} para recibir notificaciones cuando estén disponibles los recursos para una instancia transitoria. También puede utilizar la API para suministrar mediante programación un servidor virtual transitorio cuando los recursos estén disponibles. Asimismo, puede utilizar la API para detener mediante programación el suministro de instancias cuando los recursos dejen de estar disponibles. Para obtener más información, consulte [Configuración de notificaciones de reclamación automatizadas](configuring-automated-reclaim-notifications.html).

## Limitaciones
Tenga en cuenta las siguientes limitaciones antes de suministrar un servidor virtual transitorio.

* El número de instancias simultáneas soportadas forman parte de su cuota del dispositivo en toda la cuenta. Para obtener más información sobre los límites de instancias simultáneas, consulte [Preguntas frecuentes: servidores virtuales](../vsi/vsi_faqs_vs.html#concurrent).
* Las instancias transitorias no se pueden actualizar ni degradar.
* Los recursos se pueden reclamar en cualquier momento, sin notificación.
* Las instancias transitorias no pueden utilizar almacenamiento local.
* Las instancias transitorias solo utilizan almacenamiento respaldado por SAN (equilibrado, cálculo, memoria).
* Las instancias transitorias no pueden utilizar tipos basados en GPU.


## Siguientes pasos

Después de revisar y seleccionar el tipo de servidor virtual, es hora de suministrar su servidor virtual transitorio. Para empezar, revise la información siguiente:
1. [Selecciones de suministro](../vsi/vsi_public_selections.html)
2. [Suministro de instancias transitorias](../vsi/vsi_provision_transient.html)
