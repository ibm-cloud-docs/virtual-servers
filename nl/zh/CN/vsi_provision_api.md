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

# 公共虚拟服务器（带类型模板）API 示例
{: #api-python-public} 

以下信息显示了用于供应使用预设置类型模板的公共虚拟服务器实例的 REST API 示例。
{:shortdesc}

要获取更稳健的 API 示例，请参阅以下资源：
* [Softlayer_Virtual_Guest API 示例](https://softlayer.github.io/classes/softlayer_virtual_guest/)

## 使用创建对象供应公共实例
要供应使用预设置类型模板的公共虚拟服务器实例，使用 *SoftLayer_Virtual_Guest/createObject* API 服务是最简单的方法。

要使用 REST 来供应公共虚拟服务器实例，请在请求主体中使用以下 JSON 将 POST 请求提交到 https://api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/createObject.json。

### JSON 请求主体 1
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

## 使用下单对象供应公共实例
使用 *SoftLayer_Product_Order/paceOrder* API 服务可供应使用预设置类型模板的公共虚拟服务器。

要使用 REST 来供应公共虚拟服务器，请在请求主体中使用以下 JSON 将 POST 请求提交到 https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json。

**注**：价格上不需要项目描述。仅在显示要提交的产品选项时才包含项目描述。

### JSON 请求主体 2
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

## 升级公共实例
使用 *SoftLayer_Product_Order/placeOrder* API 服务可升级公共虚拟服务器。

要使用 REST 来供应公共虚拟服务器，请在请求主体中使用以下 JSON 将 POST 请求提交到 https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json。

**注**：价格上不需要项目描述。仅在显示要提交的产品选项时才包含项目描述。

### JSON 请求主体 3
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
