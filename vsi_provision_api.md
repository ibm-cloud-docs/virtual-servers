---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# API examples: Public virtual servers flavors
{: #api-rest-public}

The following information displays Rest API examples for provisioning public virtual server instances that use pre-set flavors.
{:shortdesc}

For more robust API examples, see the following resources:
* [Softlayer_Virtual_Guest API examples](https://softlayer.github.io/classes/softlayer_virtual_guest/)

## Provisioning a public instance using Create Object
The *SoftLayer_Virtual_Guest/createObject* API service is the simplest way to provision a public virtual server instance that uses pre-set flavors.

Not applicable for transient instances.
{:tip}

To provision a public virtual server instance using REST, a POST request would be submitted to https://api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/createObject.json with the following JSON in the request body.

### JSON Request Body 1
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

## Provisioning a public instance using Place Order Object
Provisioning a public virtual server that uses pre-set flavors is done using the *SoftLayer_Product_Order/placeOrder* API service.

Not applicable for transient instances.
{:tip}

To provision a public virtual server using REST, a POST request would be submitted to https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json with the below JSON in the request body.

**Note:** The item descriptions are not required on the prices. They are included only to show the product options being submitted.

### JSON Request Body 2
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

## Upgrading public instances
Upgrading a public virtual server is done using the *SoftLayer_Product_Order/placeOrder* API service.

Not applicable for transient instances.
{:tip}

To provision a public virtual server using REST, a POST request would be submitted to https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json with the below JSON in the request body.

**Note:** The item descriptions are not required on the prices. They are included only to show the product options being submitted.

### JSON Request Body 3
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
## Provisioning a transient instance using Create Object
{: #api-rest-transient}

The *SoftLayer_Virtual_Guest/createObject* API service is the simplest way to provision a transient virtual server instance.

To provision a transient virtual server instance using REST, a POST request would be submitted to https://api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/createObject.json with the following JSON in the request body.

### JSON Request Body 4
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
