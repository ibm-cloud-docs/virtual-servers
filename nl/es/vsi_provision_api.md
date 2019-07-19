---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:table: .aria-labeledby="caption"}

# Ejemplos de API: perfiles de servidores virtuales públicos
{: #api-rest-public}

La información siguiente muestra ejemplos de la API REST para instancias de servidor virtual público que utilizan perfiles predefinidos.
{:shortdesc}

Para ver ejemplos de API más potentes, consulte los siguientes recursos:
* [Ejemplos de la API Softlayer_Virtual_Guest ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/classes/softlayer_virtual_guest/)
* [Obtención de una lista de perfiles ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://softlayer.github.io/article/vsiflavors/)

## Suministro de una instancia pública mediante Crear objeto
El servicio de la API *SoftLayer_Virtual_Guest/createObject* constituye el modo más sencillo de suministrar una instancia de servidor virtual público que utilice perfiles predefinidos.

No aplicable a instancias transitorias.
{:tip}

Para suministrar una instancia de servidor virtual público mediante REST, se debe enviar una solicitud POST a https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ con el siguiente JSON en el cuerpo de la solicitud.

El cuerpo de solicitud JSON siguiente es un ejemplo genérico. 
{:note}

### Cuerpo 1 de solicitud JSON
```
{
    "parameters":[
        {
            "hostname": "public-01-mex01",
            "domain": "softlayer.local",
            "datacenter": {
                "name": "mex01"
            },
            "operatingSystemReferenceCode": "CENTOS_LATEST",
            "networkComponents": [
                {
                    "maxSpeed": 100
                }
            ],
            "hourlyBillingFlag": false,
            "supplementalCreateObjectOptions": {
                "flavorKeyName": "B1_1X2X25"
            }
        }
    ]
}
```

## Suministro de una instancia pública mediante Colocar objeto de pedido
El suministro de un servidor virtual público que utilice perfiles predefinidos se realiza mediante el servicio de la API *SoftLayer_Product_Order/placeOrder*.

No aplicable a instancias transitorias.
{:tip}

Para suministrar un servidor virtual público mediante REST, se debe enviar una solicitud POST a https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ con el siguiente JSON en el cuerpo de la solicitud.

Las descripciones de elementos no se necesitan en los precios. Solo se incluyen para mostrar las opciones del producto que se envían.
{:note}

El cuerpo de solicitud JSON siguiente es un ejemplo genérico. 
{:note}

### Cuerpo 2 de solicitud JSON
```
{
    "parameters": [
        {
            "location": "449600",
            "packageId": 835,
            "presetId": 554,
            "prices": [
                {
                    "id": 45466,
                    "item": {
                        "description": "CentOS 7.x - Instalación mínima (64 bits)"
                    }
                },
                {
                    "id": 2202,
                    "item": {
                        "description": "25 GB (SAN)"
                    }
                },
                {
                    "id": 905,
                    "item": {
                        "description": "Rearranque / Consola remota"
                    }
                },
                {
                    "id": 273,
                    "item": {
                        "description": "100 Mbps de enlaces ascendentes de red pública y privada"
                    }
                },
                {
                    "id": 50367,
                    "item": {
                        "description": "250 GB de ancho de banda"
                    }
                },
                {
                    "id": 21,
                    "item": {
                        "description": "1 dirección IP"
                    }
                },
                {
                    "id": 55,
                    "item": {
                        "description": "Host Ping"
                    }
                },
                {
                    "id": 57,
                    "item": {
                        "description": "Correo electrónico e incidencia"
                    }
                },
                {
                    "id": 58,
                    "item": {
                        "description": "Notificación automática"
                    }
                },
                {
                    "id": 420,
                    "item": {
                        "description": "Número ilimitado de usuarios de SSL VPN y 1 usuario de PPTP VPN por cuenta"
                    }
                },
                {
                    "id": 418,
                    "item": {
                        "description": "Evaluación y notificación de vulnerabilidades Nessus"
                    }
                }
            ],
            "quantity": 1,
            "useHourlyPricing": false,
            "virtualGuests": [
                {
                    "domain": "softlayer.local",
                    "hostname": "public-01-mex01"
                }
            ],
            "complexType": "SoftLayer_Container_Product_Order_Virtual_Guest"
        }
    ]
}
```

## Actualización de instancias públicas
La actualización de un servidor virtual público se realiza mediante el servicio de la API *SoftLayer_Product_Order/placeOrder*.

No aplicable a instancias transitorias.
{:tip}

Para suministrar un servidor virtual público mediante REST, se debe enviar una solicitud POST a https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ con el siguiente JSON en el cuerpo de la solicitud.

Las descripciones de elementos no se necesitan en los precios. Solo se incluyen para mostrar las opciones del producto que se envían.
{:note}

El cuerpo de solicitud JSON siguiente es un ejemplo genérico. 
{:note}

### Cuerpo 3 de solicitud JSON
```
{
    "parameters":[
        {
            "complexType": "SoftLayer_Container_Product_Order_Virtual_Guest_Upgrade",
            "presetId": 494,
            "prices": [
                {
                    "id":"274",
                    "item": {
                        "description": "1 Gbps de enlaces ascendentes de red pública y privada"
                    },
                    "categories": [
                        {
                            "categoryCode": "port_speed"
                        }
                    ]
                }
            ],
            "properties": [
                {
                    "name": "MAINTENANCE_WINDOW",
                    "value": "2017-07-20T13:48:31-05:00"
                }
            ],
            "virtualGuests": [
                {
                    "id": 36189167
                }
            ]
        }
    ]
}
```
## Suministro de una instancia transitoria mediante Crear objeto
{: #api-rest-transient}

El servicio de la API *SoftLayer_Virtual_Guest/createObject* constituye el modo más sencillo de suministrar una instancia de servidor virtual transitorio.

Para suministrar una instancia de servidor virtual transitorio mediante REST, se debe enviar una solicitud POST a https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ con el siguiente JSON en el cuerpo de la solicitud.

El cuerpo de solicitud JSON siguiente es un ejemplo genérico. 
{:note}

### Cuerpo 4 de solicitud JSON
```
{
    "parameters":[
        {
            "hostname": "sample-transient-public",
            "domain": "softlayer.local",
            "datacenter": {
                "name": "mex01"
            },
            "operatingSystemReferenceCode": "CENTOS_LATEST",
            "networkComponents": [
                {
                    "maxSpeed": 100
                }
            ],
            "supplementalCreateObjectOptions": {
                "flavorKeyName": "B1_1X2X25"
            },
            "transientGuestFlag": true
        }
    ]
}
```
