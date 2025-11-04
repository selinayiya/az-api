---
title: Get Position Information (Maker)
position_number: 20
type: get
description: /az/future/cache/v1/positions
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: Trading pair (see the position information of all trading pairs if don't pass parameters)
        ranges:
content_markdown: |-
              #### **Note**

              For Market Makers Only

              #### **Limit Flow Rules**

              200/s/apikey
left_code_blocks:
    -
        code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/user/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
        title: Java
        language: java
right_code_blocks:
    - code_block: |-
        {
          "error": {
            "code": "",
            "msg": ""
          },
          "msgInfo": "",
          "result": [
            {
                "symbol": "btc_usdt",        //Trading pair
                "positionType": "CROSSED",   //Position type
                "positionSide": "LONG",      //Position side
                "leverage": 20,              //Leverage
                "positionSize": "7000",      //Position quantity (Cont)
                "closeOrderSize": "0",       //Quantity of open order (Cont)
                "availableCloseSize": "7000",  //Available quantity (Cont)
                "entryPrice": "110000",        //Average opening price
                "openOrderSize": "0",          //Opening warehouse orders occupied
                "isolatedMargin": "3850",      //Isolated Margin
                "openOrderMarginFrozen": "0",  //Occupied open position margin
                "realizedProfit": "880.05305855",  //Realized profit and loss
                "closeProfit": "0",                //Closed Profit and Loss
                "totalFee": "-77.846426",          //Total fee
                "totalFundFee": "5857.22457151",   //Total fund fee
                "contractSize": "0.0001",          //Contract multiplier(face value)
                "markPrice": "106896.5",           //Mark Price
                "updatedTime": "1762221600282"
            }
          ],
          "returnCode": 0
        }
      title: Response
      language: json
---
