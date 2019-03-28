---

copyright:
  years: 2018, 2019
lastupdated: "2019-03-01"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# Visualización de la característica de suspensión de facturación
{: #viewing-suspend-billing-feature}

Puede ver si su instancia de servidor virtual admite la característica de suspensión de facturación en {{site.data.keyword.slportal_full}} o a través de {{site.data.keyword.slapi_short}}.

## Visualización de la característica de suspensión de facturación en el portal de clientes
Para determinar si su instancia de servidor virtual admite la característica de suspensión de facturación en {{site.data.keyword.slportal}}, utilice los siguientes pasos:

1. Inicie una sesión en el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
2. En el menú **Dispositivos**, seleccione **Lista de dispositivos**.
3. En la **Lista de dispositivos**, haga clic en el nombre de su instancia de servidor virtual.
4. En el separador **Configuración** en la sección **General**, puede ver si su instancia de servidor virtual admite la característica de suspensión de facturación.

| Campo                                 | Valor                     |
| --------------------------------------| ------------------------- |
| Suspensión de facturación: Habilitada en apagar | La característica está soportada.     |
| Suspensión de facturación: No disponible          | La característica no está soportada. |
{: caption="Tabla 1. Detalles de la suspensión de facturación" caption-side="top"}

## Visualización de la característica de suspensión de facturación a través de la API de Softlayer

El siguiente mandato es una solicitud de ejemplo de verificación de si la instancia del servidor virtual admite la característica de suspensión de facturación en {{site.data.keyword.slapi_short}}.

**Nota**: La solicitud y respuesta JSON siguientes son un ejemplo genérico.

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
1. [Acerca de la suspensión de facturación](/docs/vsi?topic=virtual-servers-requirements)
2. [Gestión de servidores virtuales](/docs/vsi?topic=virtual-servers-managing-virtual-servers)
