---



copyright:
  years: 2017
lastupdated: "2017-04-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Exemples d'API de serveurs virtuels publics (avec versions)
{: #api-python-public} 

Des exemples d'API REST permettant de mettre à disposition des instances de serveur virtuel public qui utilisent des versions prédéfinies sont présentés ci-dessous.
{:shortdesc}

Pour accéder à des exemples d'API plus robustes, voir les ressources suivantes :
* [Softlayer_Virtual_Guest API examples](https://softlayer.github.io/classes/softlayer_virtual_guest/)

## Mise à disposition d'une instance publique en utilisant Create Object
Le service d'API *SoftLayer_Virtual_Guest/createObject* constitue le meilleur moyen de mettre à disposition une instance de serveur virtuel public qui utilise des versions prédéfinies.

Pour mettre à disposition une instance de serveur virtuel public en utilisant REST, une demande POST est soumise à https://api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/createObject.json avec l'élément JSON suivant dans le corps de la demande.

### Corps de demande JSON 1
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

## Mise à disposition d'une instance publique en utilisant Place Order Object
La mise à disposition d'un serveur virtuel public qui utilise des versions prédéfinies est effectuée en utilisant le service d'API *SoftLayer_Product_Order/placeOrder*.

Pour mettre à disposition un serveur virtuel public en utilisant REST, une demande POST est soumise à https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json avec l'élément JSON suivant dans le corps de la demande.

**Remarque :** Les descriptions d'élément ne sont pas requises sur les prix. Elles sont incluses uniquement pour afficher les options de produit soumises.

### Corps de demande JSON 2
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

## Mise à niveau d'instances publiques
La mise à niveau d'un serveur virtuel public est effectuée à l'aide du service d'API *SoftLayer_Product_Order/placeOrder*.

Pour mettre à disposition un serveur virtuel public en utilisant REST, une demande POST est soumise à https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json avec l'élément JSON suivant dans le corps de la demande.

**Remarque :** Les descriptions d'élément ne sont pas requises sur les prix. Elles sont incluses uniquement pour afficher les options de produit soumises.

### Corps de demande JSON 3
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
                        "description": "1 Gbps Public & Private Network Uplinks"
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
