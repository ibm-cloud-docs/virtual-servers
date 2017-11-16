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

# 공용 가상 서버(특색 포함) API 예
{: #api-python-public} 

다음 정보는 사전 설정된 특색을 사용하는 공용 가상 서버 인스턴스의 프로비저닝에 대한 Rest API 예를 보여줍니다.
{:shortdesc}

더 안정적인 API 예는 다음 자원을 참조하십시오. 
* [Softlayer_Virtual_Guest API 예](https://softlayer.github.io/classes/softlayer_virtual_guest/)

## 오브젝트 작성을 사용한 공용 인스턴스 프로비저닝
*SoftLayer_Virtual_Guest/createObject* API 서비스는 사전 설정된 특색을 사용하는 공용 가상 서버 인스턴스를 프로비저닝하는 가장 간단한 방법입니다. 

REST를 사용하여 공용 가상 서버 인스턴스를 프로비저닝하는 경우에는 요청 본문에 다음 JSON을 포함하는 POST 요청이 https://api.softlayer.com/rest/v3/SoftLayer_Virtual_Guest/createObject.json에 제출됩니다. 

### JSON 요청 본문 1
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

## 주문 발주 오브젝트를 사용한 공용 인스턴스 프로비저닝
사전 설정된 특색을 사용하는 공용 가상 서버 프로비저닝은 *SoftLayer_Product_Order/placeOrder* API 서비스를 사용하여 수행됩니다. 

REST를 사용하여 공용 가상 서버를 프로비저닝하는 경우에는 요청 본문에 아래 JSON을 포함하는 POST 요청이 https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json에 제출됩니다. 

**참고:** 가격에서 항목 설명은 필수가 아닙니다. 이들은 제출되는 제품 옵션을 표시하기 위해서만 추가되었습니다. 

### JSON 요청 본문 2
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

## 공용 인스턴스 업그레이드
공용 가상 서버 업그레이드는 *SoftLayer_Product_Order/placeOrder* API 서비스를 사용하여 수행됩니다. 

REST를 사용하여 공용 가상 서버를 프로비저닝하는 경우에는 요청 본문에 아래 JSON을 포함하는 POST 요청이 https://api.softlayer.com/rest/v3/SoftLayer_Product_Order/placeOrder.json에 제출됩니다. 

**참고:** 가격에서 항목 설명은 필수가 아닙니다. 이들은 제출되는 제품 옵션을 표시하기 위해서만 추가되었습니다. 

### JSON 요청 본문 3
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
