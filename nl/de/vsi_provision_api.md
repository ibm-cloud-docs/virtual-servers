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

# API-Beispiele: Profile öffentlicher virtueller Server
{: #api-rest-public}

Die folgenden Informationen enthalten REST-API-Beispiel für die Bereitstellung öffentlicher virtueller Serverinstanzen, die vordefinierte Profile verwenden.
{:shortdesc}

Besonders leistungsfähige API-Beispiele finden Sie in den folgenden Ressourcen:
* [API-Beispiele für Softlayer_Virtual_Guest ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/classes/softlayer_virtual_guest/)
* [Profilliste abrufen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/article/vsiflavors/)

## Öffentliche Instanz mit dem Objekt 'create' bereitstellen
Der API-Service *SoftLayer_Virtual_Guest/createObject* ist die einfachste Methode, um eine öffentliche virtuelle Serverinstanz bereitzustellen, die vordefinierte Profile verwendet.

Nicht zutreffend für transiente Instanzen.
{:tip}

Zum Bereitstellen einer öffentlichen virtuellen Serverinstanz mit REST wird eine POST-Anforderung an https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ übergeben, die den folgenden JSON-Code im Anforderungshauptteil enthält.

Der folgende JSON-Anforderungshauptteil stellt ein generisches Beispiel dar.
{:note}

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
Die Bereitstellung eines öffentlichen virtuellen Servers, der vordefinierte Profile verwendet, erfolgt mit dem API-Service *SoftLayer_Product_Order/placeOrder*.

Nicht zutreffend für transiente Instanzen.
{:tip}

Zum Bereitstellen eines öffentlichen virtuellen Servers mit REST wird eine POST-Anforderung an https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ übergeben, die den folgenden JSON-Code im Anforderungshauptteil enthält.

Die Artikelbezeichnungen sind für die Preise nicht erforderlich. Sie sind nur angegeben, um deutlich zu machen, welche Produktoptionen übergeben werden.
{:note}

Der folgende JSON-Anforderungshauptteil stellt ein generisches Beispiel dar.
{:note}

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

Nicht zutreffend für transiente Instanzen.
{:tip}

Zum Bereitstellen eines öffentlichen virtuellen Servers mit REST wird eine POST-Anforderung an https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ übergeben, die den folgenden JSON-Code im Anforderungshauptteil enthält.

Die Artikelbezeichnungen sind für die Preise nicht erforderlich. Sie sind nur angegeben, um deutlich zu machen, welche Produktoptionen übergeben werden.
{:note}

Der folgende JSON-Anforderungshauptteil stellt ein generisches Beispiel dar.
{:note}

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
## Transiente Instanz mit dem Objekt 'create' bereitstellen
{: #api-rest-transient}

Der API-Service *SoftLayer_Virtual_Guest/createObject* ist die einfachste Methode zum Bereitstellen einer transienten virtuellen Serverinstanz.

Zum Bereitstellen einer transienten virtuellen Serverinstanz mit REST wird eine POST-Anforderung an https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ übergeben, die den folgenden JSON-Code im Anforderungshauptteil enthält.

Der folgende JSON-Anforderungshauptteil stellt ein generisches Beispiel dar.
{:note}

### JSON-Anforderungshauptteil 4
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
