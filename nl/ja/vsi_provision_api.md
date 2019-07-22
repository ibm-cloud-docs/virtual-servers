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

# API の例: パブリック仮想サーバー・プロファイル
{: #api-rest-public}

以下の情報は、事前設定プロファイルを使用するパブリック仮想サーバー・インスタンスをプロビジョニングするための REST API の例を表示します。
{:shortdesc}

より堅固な API の例については、以下のリソースを参照してください。
* [Softlayer_Virtual_Guest API サンプル ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/classes/softlayer_virtual_guest/)
* [Getting a profile list ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://softlayer.github.io/article/vsiflavors/)

## Create Object を使用したパブリック・インスタンスのプロビジョニング
*SoftLayer_Virtual_Guest/createObject* API サービスは、事前設定プロファイルを使用するパブリック仮想サーバー・インスタンスをプロビジョンするための最もシンプルな方法です。

一時インスタンスには適用されません。
{:tip}

REST を使用してパブリック仮想サーバー・インスタンスをプロビジョンするために、要求本文に以下の JSON を含む POST 要求が https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ に送信されます。

次の JSON 要求本文は、一般的な例です。 
{:note}

### JSON 要求本文 1
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

## Place Order Object を使用したパブリック・インスタンスのプロビジョニング
事前設定プロファイルを使用するパブリック仮想サーバーのプロビジョニングは、*SoftLayer_Product_Order/placeOrder* API サービスを使用して行われます。

一時インスタンスには適用されません。
{:tip}

REST を使用してパブリック仮想サーバーをプロビジョンするために、要求本文に以下の JSON を含む POST 要求が https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ に送信されます。

価格に項目の説明は必要ありません。 それらは、送信する製品オプションを示すためにのみ含まれています。
{:note}

次の JSON 要求本文は、一般的な例です。 
{:note}

### JSON 要求本文 2
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

## パブリック・インスタンスのアップグレード
パブリック仮想サーバーのアップグレードは、*SoftLayer_Product_Order/placeOrder* API サービスを使用して行われます。

一時インスタンスには適用されません。
{:tip}

REST を使用してパブリック仮想サーバーをプロビジョンするために、要求本文に以下の JSON を含む POST 要求が https://softlayer.github.io/reference/services/SoftLayer_Product_Order/placeOrder/ に送信されます。

価格に項目の説明は必要ありません。 それらは、送信する製品オプションを示すためにのみ含まれています。
{:note}

次の JSON 要求本文は、一般的な例です。 
{:note}

### JSON 要求本文 3
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
## Create Object を使用した一時インスタンスのプロビジョニング
{: #api-rest-transient}

*SoftLayer_Virtual_Guest/createObject* API サービスは、一時仮想サーバー・インスタンスをプロビジョンするための最も簡単な方法です。

REST を使用して一時仮想サーバー・インスタンスをプロビジョンするために、要求本文に以下の JSON を含む POST 要求が https://softlayer.github.io/reference/services/SoftLayer_Virtual_Guest/createObject/ に送信されます。

次の JSON 要求本文は、一般的な例です。 
{:note}

### JSON 要求本文 4
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
