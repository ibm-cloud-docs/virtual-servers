---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-28"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Visualización de la característica de suspensión de facturación
{: #viewing-suspend-billing-feature}

## Antes de empezar
En primer lugar, acceda al menú de dispositivo y asegúrese de que tiene los permisos de cuenta correctos para completar la tarea. 

* Acceda al menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos. 

Para obtener más información sobre los permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/vsi?topic=virtual-servers-managing-device-access).

## Visualización de la característica de suspensión de facturación 
Para determinar si su instancia de servidor virtual admite la característica de suspensión de facturación, utilice los siguientes pasos:

1. En el menú **Dispositivos**, seleccione **Lista de dispositivos**. 
2. En la **Lista de dispositivos**, haga clic en el nombre de su instancia de servidor virtual. 
3. En la sección **Detalles de la instancia**, puede ver si la instancia de servidor virtual admite la característica de suspensión de la facturación. 

| Campo                                 | Valor                     |
| --------------------------------------| ------------------------- |
| Facturación suspendida: Habilitada al apagar | La característica está soportada.     |
| Facturación suspendida: No disponible          | La característica no está soportada. |
{: caption="Tabla 1. Detalles de la suspensión de facturación" caption-side="top"}

## Visualización de la característica de suspensión de facturación a través de la API de SoftLayer

El siguiente mandato es una solicitud de ejemplo de verificación de si la instancia del servidor virtual admite la característica de suspensión de facturación a través de la {{site.data.keyword.slapi_short}}.

La solicitud y la respuesta JSON siguiente es un ejemplo genérico. 
{:note}

```
curl -X GET \
 https://$SOFTLAYER_USERNAME:$SOFTLAYER_API_KEY@api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/<VSI ID>/getAttributes.json
```

A continuación, encontrarás una respuesta JSON de ejemplo a la solicitud:

```
[{"value":"1","type":{"keyname":"SUSPENDED_BILLING","name":"Suspended Billing"}}]
```

Para obtener más información, consulte la [documentación de API SLDN ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/getAttributes/){: new_window}.

## Siguientes pasos

Para saber más sobre la característica de suspensión de facturación, revise la siguiente información:
1. [Suspensión de la facturación](/docs/vsi?topic=virtual-servers-about-suspend-billing#about-suspend-billing)
2. [Gestión de servidores virtuales](/docs/vsi?topic=virtual-servers-managing-virtual-servers#managing-virtual-servers)

