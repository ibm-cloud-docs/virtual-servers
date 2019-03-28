---

copyright:
  years: 2018
lastupdated: "2018-10-31"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Grupos de colocación
{: #placement-groups}

Con los grupos de colocación de {{site.data.keyword.BluVirtServers}}, puede utilizar instancias públicas para crear alta disponibilidad dentro de un centro de datos o proporcionar un nivel adicional de tolerancia de errores dentro de un despliegue mayor.
{:shortdesc}

Cree su grupo de colocación y, a continuación, asigne hasta 5 nuevas instancias de servidor virtual. Con la regla de dispersión, se suministra a cada uno de los servidores virtuales con hosts físicos diferentes.

Para comenzar, realice estos pasos:

1. Desde el navegador, abra [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){:new_window} e inicie sesión en su cuenta.
2. En la página Grupos de colocación, haga clic en **Agregar grupo de colocación**.
3. Introduzca un nombre, una descripción y un centro de datos para el grupo de colocación y haga clic en **Agregar**.
4. Localice la sección **Pedido** y pulse **Dispositivos**.
5. En la página de Dispositivos, haga clic en **Por hora** o **Mensual** para una de las ofertas de servidor virtual.
6. Complete la información necesaria y pulse **Añadir a pedido**. Se abrirá la página de pago.
7. Puede seleccionar cualquier grupo de colocación. **Dispersar** significa que las instancias estarán en hardware físico diferente.
8. Por último, pulse **Enviar pedido**.

##Limitaciones
Las instancias existentes no se pueden agregar a un grupo de colocación. Solo puede agregar una instancia de servidor virtual a un grupo de colocación en el suministro.

Para eliminar una instancia de un grupo de colocación, debe eliminar o reclamar la instancia.

## Siguientes pasos

Para crear y gestionar nuevos grupos de colocación, consulte [Gestión de grupos de colocación](/docs/vsi?topic=virtual-servers-vsi_managing_placegroup).
