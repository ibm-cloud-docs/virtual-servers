---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-25"

subcollection: virtual-servers

---

{{site.data.keyword.attribute-definition-list}}

# API examples: Public virtual servers profiles
{: #api-rest-public}

The following information displays Rest API examples for provisioning public virtual servers that use pre-set profiles.
{: shortdesc}

For more robust API examples, see the following resources:
* [Softlayer_Virtual_Guest API examples](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/){: external}
* [Getting a profile list](https://sldn.softlayer.com/article/vsiflavors/){: external}

## Provisioning a public virtual server with Create Object
{: #provisioning-a-public-instance-using-create-object}

The `SoftLayer_Virtual_Guest/createObject` API service is the simplest way to provision a public virtual server that uses pre-set profiles.

Not applicable for transient virtual servers.
{: tip}

To provision a public virtual server by using REST, a POST request would be submitted to https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ with the following JSON in the request body.

The following JSON request body is a generic example.

### JSON Request Body 1
{: #json-request-body-1}

```bash
{
    "parameters":[
        {
            "hostname": "public-01-dal10",
            "domain": "softlayer.local",
            "datacenter": {
                "name": "dal10"
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
{: codeblock}

## Provisioning a public virtual server with Place Order Object
{: #provisioning-a-public-instance-using-place-order-object}

Provisioning a public virtual server that uses pre-set profiles is done by using the `SoftLayer_Product_Order/placeOrder` API service.

Not applicable for transient virtual servers.
{: tip}

To provision a public virtual server by using REST, a POST request would be submitted to [Place order](https://sldn.softlayer.com/reference/services/SoftLayer_Product_Order/placeOrder/){: external} with the following JSON in the request body.

The item descriptions are not required on the prices. They are included only to show the product options that are being submitted.
{: note}

The following JSON request body is a generic example.

### JSON Request Body 2
{: #json-request-body-2}

```bash
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
                }
            ],
            "quantity": 1,
            "useHourlyPricing": false,
            "virtualGuests": [
                {
                    "domain": "softlayer.local",
                    "hostname": "public-01-dal10"
                }
            ],
            "complexType": "SoftLayer_Container_Product_Order_Virtual_Guest"
        }
    ]
}
```
{: codeblock}

## Upgrading public virtual servers
{: #upgrading-public-instances}

Upgrading a public virtual server is done by using the `SoftLayer_Product_Order/placeOrder` API service.

Not applicable for transient virtual servers.
{: tip}

To provision a public virtual server by using REST, a POST request would be submitted to [Place order](https://sldn.softlayer.com/reference/services/SoftLayer_Product_Order/placeOrder/){: external} with the following JSON in the request body.

The item descriptions are not required on the prices. They are included only to show the product options that are being submitted.
{: note}

The following JSON request body is a generic example.

### JSON Request Body 3
{: #json-request-body-3}

```bash
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
{: codeblock}

## Provisioning a transient virtual server with Create Object
{: #api-rest-transient}

The `SoftLayer_Virtual_Guest/createObject` API service is the simplest way to provision a transient virtual server.

To provision a transient virtual server by using REST, a POST request would be submitted to [Create object](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest/createObject/){: external} with the following JSON in the request body.

The following JSON request body is a generic example.

### JSON Request Body 4
{: #json-request-body-4}

```bash
{
    "parameters":[
        {
            "hostname": "sample-transient-public",
            "domain": "softlayer.local",
            "datacenter": {
                "name": "dal10"
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
{: codeblock}
