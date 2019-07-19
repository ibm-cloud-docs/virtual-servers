---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords: auto scale, virtual servers

subcollection: virtual-servers

---

{:note: .note}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Acerca del escalado automático
{: #about-auto-scale}

El escalado automático de instancias de servidor virtual de {{site.data.keyword.cloud}} le proporciona la capacidad de automatizar el proceso de escalado manual asociado con la adición o eliminación de instancias para dar soporte a las aplicaciones empresariales. Esto le permite configurar nuevas instancias de forma automática a medida que se necesitan más recursos y, posteriormente, dichas instancias se concluirán y eliminarán cuando disminuya la carga adicional. El escalado automático utiliza grupos para contener las políticas que cambian cómo se expande o se contrae su entorno. Estas políticas utilizan acciones para añadir o eliminar el servidor virtual en función de las necesidades de su negocio y aplicación. 
{:shortdesc}

El escalado automático habilita las características siguientes:

* Aumento automático y transparente del número de instancias cuando se necesitan más recursos debido a la demanda
* Reducción automática y transparente del número de instancias, eliminando recursos innecesarios cuando cae la demanda (ahorrando así dinero)
* Desencadenantes flexibles del escalado: porcentaje de CPU, ancho de banda público y privado saliente, ancho de banda público y privado entrante
* Actualizaciones de estado prácticamente en tiempo real para las actividades de escalado en grupos
* Integración opcional de LAN virtual (VLAN) y equilibradores de carga local

Hay dos soluciones empresariales comunes a las que se puede aplicar el escalado automático:

| Solución | Descripción |
| -------- | ----------- |
| [Escalado basado en planificación](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling) | El escalado basado en planificación se puede utilizar para configurar políticas para los picos de uso basados en tiempo, como los fines de semana o los días festivos. El escalado basado en planificación se puede utilizar cuando una empresa espera que el tráfico llegue a un pico, por ejemplo, un sitio de red social que requiere más recursos según una planificación. |
| [Escalado basado en recursos](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling) | La planificación basada en recursos se puede utilizar para configurar políticas para picos irregulares, basados en uso de recursos. Se pueden producir picos irregulares en el tráfico cuando hay una demanda por obtener un producto para comercializar o un sitio de comercio electrónico está teniendo una venta y se necesitan recursos para mantener los tiempos de respuesta. |
{: caption="Tabla 1. Soluciones de escalado automático" caption-side="top"}

Si no es el administrador de la cuenta, su cuenta de usuario debe incluir el permiso para utilizar el escalado automático. El administrador de la cuenta puede otorgar permiso al usuario desde la consola de {{site.data.keyword.cloud_notm}}. Para obtener más información sobre la actualización de permisos, consulte [Configuración de permisos de usuario para el escalado automático](/docs/vsi?topic=virtual-servers-user-permissions-required-to-use-auto-scale).
{:note}


