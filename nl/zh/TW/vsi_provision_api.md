---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}

# API 範例：公用虛擬伺服器設定檔
{: #api-rest-public}

下列資訊所顯示的 REST API 範例用來佈建使用預設設定檔的公用虛擬伺服器實例。
{:shortdesc}

如需更健全的 API 範例，請參閱下列資源：
* [Softlayer_Virtual_Guest API 範例 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://softlayer.github.io/classes/softlayer_virtual_guest/)
* [取得設定檔清單 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://softlayer.github.io/article/vsiflavors/)

## 使用建立物件佈建公用實例
*SoftLayer_Virtual_Guest/createObject* API 服務是佈建使用預設設定檔的公用虛擬伺服器實例的最簡單方式。

不適用於暫時性實例。
{:tip}

若要使用 REST 來佈建公用虛擬伺服器實例，會將 POST 要求提交至 https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ 並且在要求內文中使用下列 JSON。

### JSON 要求內文 1
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

## 使用下單物件佈建公用實例
佈建使用預設設定檔的公用虛擬伺服器的方式是使用 *SoftLayer_Product_Order/placeOrder* API 服務。

不適用於暫時性實例。
{:tip}

若要使用 REST 來佈建公用虛擬伺服器，會將 POST 要求提交至 https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ 並且在要求內文中使用下列 JSON。

**附註：**價格上不需要項目說明。包含它們的目的只是要顯示所提交的產品選項。

### JSON 要求內文 2
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

## 升級公用實例
升級公用虛擬伺服器的方式是使用 *SoftLayer_Product_Order/placeOrder* API 服務。

不適用於暫時性實例。
{:tip}

若要使用 REST 來佈建公用虛擬伺服器，會將 POST 要求提交至 https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ 並且在要求內文中使用下列 JSON。

**附註：**價格上不需要項目說明。包含它們的目的只是要顯示所提交的產品選項。

### JSON 要求內文 3
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
## 使用建立物件來佈建暫時性實例
{: #api-rest-transient}

*SoftLayer_Virtual_Guest/createObject* API 服務是佈建暫時性虛擬伺服器實例的最簡單方式。

若要使用 REST 來佈建暫時性虛擬伺服器實例，會將 POST 要求提交至 https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ 並且在要求內文中使用下列 JSON。

### JSON 要求內文 4
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
