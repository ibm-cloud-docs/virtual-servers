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

# Exemplos de API: perfis de servidores virtuais públicos
{: #api-rest-public}

As informações a seguir exibem exemplos da API de REST para provisionar instâncias de servidor virtual público que usam perfis pré-configurados.
{:shortdesc}

Para exemplos de API mais robustos, veja os recursos a seguir:
* [Exemplos da API Softlayer_Virtual_Guest ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/classes/softlayer_virtual_guest/)
* [Obtendo uma lista de perfis ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://softlayer.github.io/article/vsiflavors/)

## Provisionando uma instância pública usando Criar objeto
O serviço de API *SoftLayer_Virtual_Guest/createObject* é a maneira mais simples de provisionar uma instância de servidor virtual público que usa perfis pré-configurados.

Não aplicável para instâncias temporárias.
{:tip}

Para provisionar uma instância de servidor virtual público usando REST, uma solicitação de POST seria enviada para https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ com o JSON a seguir no corpo da solicitação.

O corpo da solicitação JSON a seguir é um exemplo genérico. 
{:note}

### Corpo da solicitação JSON 1
```
{
    "parameters":[ {
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

## Provisionando uma instância pública usando Colocar objeto de ordem
A provisão de um servidor virtual público que usa perfis pré-configurados é feita usando o serviço de API *SoftLayer_Product_Order/placeOrder*.

Não aplicável para instâncias temporárias.
{:tip}

Para provisionar um servidor virtual público usando REST, uma solicitação de POST seria enviada para https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ com o JSON abaixo no corpo da solicitação.

As descrições de itens não são necessárias nos preços. Eles são incluídos somente para mostrar as opções do produto que estão sendo enviadas.
{:note}

O corpo da solicitação JSON a seguir é um exemplo genérico. 
{:note}

### Corpo da solicitação JSON 2
```
{
    "parameters":[ {
            "location": "449600",
            "packageId": 835,
            "presetId": 554,
            "prices": [
                {
                    "id": 45466,
                    "item": {
                        "description": "CentOS 7.x - Minimal Install (64 bit)"
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
                        "description": "Reboot / Remote Console"
                    }
                },
                {
                    "id": 273,
                    "item": {
                        "description": "100 Mbps Public & Private Network Uplinks"
                    }
                },
                {
                    "id": 50367,
                    "item": {
                        "description": "250 GB Bandwidth"
                    }
                },
                {
                    "id": 21,
                    "item": {
                        "description": "1 IP Address"
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
                        "description": "Email and Ticket"
                    }
                },
                {
                    "id": 58,
                    "item": {
                        "description": "Automated Notification"
                    }
                },
                {
                    "id": 420,
                    "item": {
                        "description": "Unlimited SSL VPN Users & 1 PPTP VPN User per account"
                    }
                },
                {
                    "id": 418,
                    "item": {
                        "description": "Nessus Vulnerability Assessment & Reporting"
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

## Fazendo upgrade de instâncias públicas
O upgrade de um servidor virtual público é feito usando o serviço de API *SoftLayer_Product_Order/placeOrder*.

Não aplicável para instâncias temporárias.
{:tip}

Para provisionar um servidor virtual público usando REST, uma solicitação de POST seria enviada para https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ com o JSON abaixo no corpo da solicitação.

As descrições de itens não são necessárias nos preços. Eles são incluídos somente para mostrar as opções do produto que estão sendo enviadas.
{:note}

O corpo da solicitação JSON a seguir é um exemplo genérico. 
{:note}

### Corpo da solicitação JSON 3
```
{
    "parameters":[ {
            "complexType": "SoftLayer_Container_Product_Order_Virtual_Guest_Upgrade",
            "presetId": 494,
            "prices": [
                {
                    "id":"274",
                    "item": {
                        "description": "Uplinks de rede pública e privada de 1 Gbps"
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
## Provisionando uma instância temporária usando Criar objeto
{: #api-rest-transient}

O serviço de API *SoftLayer_Virtual_Guest/createObject* é a maneira mais simples de provisionar uma instância de servidor virtual temporária.

Para provisionar uma instância de servidor virtual temporária usando REST, uma solicitação de POST seria enviada para https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ com o JSON a seguir no corpo da solicitação.

O corpo da solicitação JSON a seguir é um exemplo genérico. 
{:note}

### Corpo da solicitação 4 de JSON
```
{
    "parameters":[ {
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
