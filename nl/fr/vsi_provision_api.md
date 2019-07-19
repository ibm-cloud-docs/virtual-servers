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

# Exemples d'API : profils de serveurs virtuels
{: #api-rest-public}

Des exemples d'API REST permettant de mettre à disposition des instances de serveur virtuel public qui utilisent des profils prédéfinis sont présentés ci-dessous.
{:shortdesc}

Pour accéder à des exemples d'API plus robustes, voir les ressources suivantes :
* [Exemples d'API softlayer_virtual_guest ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/classes/softlayer_virtual_guest/)
* [Obtention d'une liste de profils ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://softlayer.github.io/article/vsiflavors/)

## Mise à disposition d'une instance publique en utilisant Create Object
Le service d'API *SoftLayer_Virtual_Guest/createObject* constitue le meilleur moyen de mettre à disposition une instance de serveur virtuel public qui utilise des profils prédéfinis.

Non applicable aux instances transitoires.
{:tip}

Pour mettre à disposition une instance de serveur virtuel public en utilisant REST, une demande POST est soumise dans https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ avec l'élément JSON suivant dans le corps de la demande.

Le corps de demande JSON suivant est un exemple générique. 
{:note}

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
La mise à disposition d'un serveur virtuel public qui utilise des profils prédéfinis est effectuée en utilisant le service d'API *SoftLayer_Product_Order/placeOrder*.

Non applicable aux instances transitoires.
{:tip}

Pour mettre à disposition un serveur virtuel public en utilisant REST, une demande POST est soumise dans https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ avec l'élément JSON suivant dans le corps de la demande.

Les descriptions d'élément ne sont pas requises sur les prix. Elles sont incluses uniquement pour afficher les options de produit soumises.
{:note}

Le corps de demande JSON suivant est un exemple générique. 
{:note}

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

Non applicable aux instances transitoires.
{:tip}

Pour mettre à disposition un serveur virtuel public en utilisant REST, une demande POST est soumise dans https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ avec l'élément JSON suivant dans le corps de la demande.

Les descriptions d'élément ne sont pas requises sur les prix. Elles sont incluses uniquement pour afficher les options de produit soumises.
{:note}

Le corps de demande JSON suivant est un exemple générique. 
{:note}

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
## Mise à disposition d'une instance transitoire à l'aide de Create Object
{: #api-rest-transient}

Le service d'API *SoftLayer_Virtual_Guest/createObject* offre le meilleur moyen de mettre à disposition une instance de serveur virtuel transitoire.

Pour mettre à disposition une instance de serveur virtuel transitoire en utilisant REST, une demande POST est soumise dans https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ avec l'élément JSON suivant dans le corps de la demande.

Le corps de demande JSON suivant est un exemple générique. 
{:note}

### Corps de la demande JSON 4
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
