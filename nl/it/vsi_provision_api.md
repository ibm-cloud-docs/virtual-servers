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

# Esempi API: profili server virtuali pubblici
{: #api-rest-public}

Le seguenti informazioni visualizzano gli esempi API Rest per il provisioning delle istanze del server virtuale pubbliche che utilizzano profili preimpostati.
{:shortdesc}

Per ulteriori esempi API solidi, consulta le seguenti risorse:
* [Softlayer_Virtual_Guest API examples ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/classes/softlayer_virtual_guest/)
* [Getting a profile list ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://softlayer.github.io/article/vsiflavors/)

## Provisioning di un'istanza pubblica utilizzando Crea oggetto
Il servizio API *SoftLayer_Virtual_Guest/createObject* è il modo più semplice per eseguire il provisioning di un'istanza del server virtuale pubblica che utilizza profili preimpostati.

Non applicabile alle istanze temporanee.
{:tip}

Per eseguire il provisioning di un'istanza del server virtuale pubblica utilizzando REST, deve essere inviata una richiesta POST all'indirizzo https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ con il seguente JSON nel corpo della richiesta.

Il seguente corpo della richiesta JSON è un esempio generico.
{:note}

### Corpo richiesta JSON 1
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

## Provisioning di un'istanza pubblica utilizzando Effettua ordine oggetto
Il provisioning di un server virtuale pubblico che utilizza i profili preimpostati viene eseguito utilizzando il servizio API *SoftLayer_Product_Order/placeOrder*.

Non applicabile alle istanze temporanee.
{:tip}

Per eseguire il provisioning di un server virtuale utilizzando REST, deve essere inviata una richiesta POST all'indirizzo https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ con il seguente JSON nel corpo della richiesta.

Le descrizioni degli elementi non sono richieste sui prezzi. Vengono incluse solo per mostrare le opzioni del prodotto che stanno venendo inviate.
{:note}

Il seguente corpo della richiesta JSON è un esempio generico.
{:note}

### Corpo richiesta JSON 2
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

## Aggiornamento delle istanze pubbliche
L'aggiornamento di un server virtuale pubblico viene eseguito utilizzando il servizio API *SoftLayer_Product_Order/placeOrder*.

Non applicabile alle istanze temporanee.
{:tip}

Per eseguire il provisioning di un server virtuale utilizzando REST, deve essere inviata una richiesta POST all'indirizzo https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ con il seguente JSON nel corpo della richiesta.

Le descrizioni degli elementi non sono richieste sui prezzi. Vengono incluse solo per mostrare le opzioni del prodotto che stanno venendo inviate.
{:note}

Il seguente corpo della richiesta JSON è un esempio generico.
{:note}

### Corpo richiesta JSON 3
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
## Provisioning di un'istanza temporanea utilizzando Crea oggetto
{: #api-rest-transient}

Il servizio API *SoftLayer_Virtual_Guest/createObject* è il modo più semplice per eseguire il provisioning di un'istanza del server virtuale temporanea.

Per eseguire il provisioning di un'istanza del server virtuale temporanea utilizzando REST, deve essere inviata una richiesta POST all'indirizzo https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ con il seguente JSON nel corpo della richiesta.

Il seguente corpo della richiesta JSON è un esempio generico.
{:note}

### Corpo richiesta JSON 4
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
