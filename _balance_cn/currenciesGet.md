---
title: 获取币种信息
position_number: 1
type: get
description: /az/spot/public/currencies
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown:
left_code_blocks:
    -
        code_block:
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": [
                    {
                        "id": 2,               //币种id
                        "currency": "btc",     //币种名称
                        "displayName": "BTC",  //currency display name
                        "type": "FT",
                        "fullName": "Bitcoin", //币种全称
                        "logo": "https://a.static-global.com/1/currency/btc.png",
                        "cmcLink": "https://coinmarketcap.com/currencies/bitcoin/",
                        "weight": 99999,
                        "maxPrecision": 10,
                        "depositStatus": 0,    //充值状态(0关闭 1开放)
                        "withdrawStatus": 0,   //提现状态(0关闭 1开放)
                        "convertEnabled": 1,   //小额资产兑换开关[0=关;1=开]
                        "transferEnabled": 1,  //划转开关[0=关;1=开]
                        "isChainExist": 1,
                        "plates": [],
                        "isListing": 1,
                        "withdrawCloseReason": "CURRENCY_CLOSE_REASON_5",
                        "chainRelation": [
                            {
                                "chainId": 715,
                                "contract": "0x7130d2A12B9BCbFAe4f2634d864A1Ee1Ce3Ead9c"
                            },
                            {
                                "chainId": 5,
                                "contract": "0x9BE89D2a4cd102D8Fecc6BF9dA793be995C22541"
                            }
                        ]           
                    }
                  ]
                }
        title: Response
        language: json
---

