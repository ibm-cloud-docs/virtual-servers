---



copyright: years: 2017 lastupdated: "2017-04-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Exemplos de API de servidores virtuais públicos (com tipos)
{: #api-python-public} 

As informações a seguir exibem exemplos de API de Rest para provisionar instâncias de servidor virtual públicas que usam tipos pré-configurados.
{:shortdesc}

Para exemplos de API mais robustos, veja os recursos a seguir:
* [Exemplos de API Softlayer_Virtual_Guest](https://softlayer.github.io/classes/softlayer_virtual_guest/)

## Provisionando uma instância pública usando Criar objeto
O serviço de API *SoftLayer_Virtual_Guest/createObject* é a maneira mais simples de provisionar uma instância de servidor virtual público que usa tipos pré-configurados.

Para provisionar uma instância de servidor virtual público usando REST, uma solicitação de POST seria enviada para https://api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/createObject.json com o JSON a seguir no corpo da solicitação.

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
O fornecimento de um servidor virtual público que usa tipos pré-configurados é feito usando o serviço de API *SoftLayer_Product_Order/placeOrder*.

Para provisionar um servidor virtual público usando REST, uma solicitação de POST seria enviada para https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json com o JSON abaixo no corpo da solicitação.

**Nota:** as descrições de itens não são necessárias nos preços. Eles são incluídos somente para mostrar as opções do produto que estão sendo enviadas.

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

Para provisionar um servidor virtual público usando REST, uma solicitação de POST seria enviada para https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json com o JSON abaixo no corpo da solicitação.

**Nota:** as descrições de itens não são necessárias nos preços. Eles são incluídos somente para mostrar as opções do produto que estão sendo enviadas.

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
