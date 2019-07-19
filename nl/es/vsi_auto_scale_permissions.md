---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuración de permisos para el escalado automático
{: #user-permissions-required-to-use-auto-scale}

El acceso a las opciones de escalado automático requiere un permiso de usuario especial más allá de la capacidad de solicitar y gestionar {{site.data.keyword.virtualmachinesshort}}. Para acceder a las características de escalado automático, debe tener permiso para gestionar todos los servidores virtuales de la cuenta, además de cualquier dispositivo virtual futuro que se añada.

Si es el administrador de la cuenta y desea otorgar a los usuarios el permiso para acceder a las opciones de escalado automático, realice los pasos siguientes:

1. Inicie sesión en la página [Acceso (IAM) ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/iam#/users){: new_window} de la consola {{site.data.keyword.cloud}}. 
2. En el separador **Usuarios**, seleccione **Ver por: Mis usuarios de infraestructura clásica**.
3. Seleccione un usuario y luego pulse el separador **Infraestructura clásica**.
4. Expanda la categoría **Dispositivos** del separador **Permisos** y seleccione **Gestionar grupos de escalado automático**.
5. Pulse **Aplicar**.

## Siguientes pasos

Una vez que tenga permiso para acceder y utilizar las opciones de escalado automático, estará listo para utilizar la característica. Para empezar, revise la información siguiente:

1. [Gestión de picos de tráfico con escalado automático basado en planificación](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [Gestión de picos de tráfico con escalado automático basado en recursos](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [Preguntas frecuentes: escalado automático](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

