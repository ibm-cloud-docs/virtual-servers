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

# API-Beispiele für öffentliche virtuelle Server (mit Flavors)
{: #api-python-public} 

Die folgenden Informationen enthalten REST-API-Beispiel für die Bereitstellung öffentlicher virtueller Serverinstanzen, die vordefinierte Versionen (Flavors) verwenden.
{:shortdesc}

Besonders leistungsfähige API-Beispiele finden Sie in den folgenden Ressourcen:
* [Softlayer_Virtual_Guest - API-Beispiele](https://softlayer.github.io/classes/softlayer_virtual_guest/)

## Öffentliche Instanz mit dem Objekt 'create' bereitstellen
Der API-Service *SoftLayer_Virtual_Guest/createObject* ist die einfachste Methode, um eine öffentliche virtuelle Serverinstanz bereitzustellen, die vordefinierte Versionen (Flavors) verwendet.

Zum Bereitstellen einer öffentlichen virtuellen Serverinstanz mit REST wird eine POST-Anforderung an https://api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/createObject.json übermittelt, die den folgenden JSON-Code im Anforderungshauptteil enthält.

### JSON-Anforderungshauptteil 1
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

## Öffentliche Instanz mit dem Objekt 'placeOrder' bereitstellen
Die Bereitstellung eines öffentlichen virtuellen Servers, der vordefinierte Versionen (Flavors) verwendet, erfolgt mit dem API-Service *SoftLayer_Product_Order/placeOrder*.

Zum Bereitstellen eines öffentlichen virtuellen Servers mit REST wird eine POST-Anforderung an https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json übergeben, die den folgenden JSON-Code im Anforderungshauptteil enthält.

**Hinweis:** Die Artikelbezeichnungen sind in den Preisen nicht erforderlich. Sie sind nur angegeben, um deutlich zu machen, welche Produktoptionen übergeben werden.

### JSON-Anforderungshauptteil 2
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

## Upgrade für öffentliche Instanzen durchführen
Die Durchführung eines Upgrades für einen öffentlichen virtuellen Server erfolgt mit dem API-Service *SoftLayer_Product_Order/placeOrder*.

Zum Bereitstellen eines öffentlichen virtuellen Servers mit REST wird eine POST-Anforderung an https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json übergeben, die den folgenden JSON-Code im Anforderungshauptteil enthält.

**Hinweis:** Die Artikelbezeichnungen sind in den Preisen nicht erforderlich. Sie sind nur angegeben, um deutlich zu machen, welche Produktoptionen übergeben werden.

### JSON-Anforderungshauptteil 3
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
