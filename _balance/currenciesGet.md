---
title: Get currency information
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
                      "id": 2,               //currency id
                      "currency": "btc",     //currency name
                      "displayName": "BTC",  //currency display name
                      "type": "FT",
                      "fullName": "Bitcoin", //full name
                      "logo": "https://a.static-global.com/1/currency/btc.png",
                      "cmcLink": "https://coinmarketcap.com/currencies/bitcoin/",
                      "weight": 99999,
                      "maxPrecision": 10,
                      "depositStatus": 0,    //Recharge status(0 close 1 open)
                      "withdrawStatus": 0,   //Withdrawal status(0 close 1 open)
                      "convertEnabled": 1,   //Small asset exchange switch[0=close;1=open]
                      "transferEnabled": 1,  //swipe switch[0=close;1=open]
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

