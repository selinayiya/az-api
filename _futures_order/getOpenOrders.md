---
title: See Open Orders (maker)
position_number: 9
type: get
description: /az/future/cache/v1/open-orders
parameters:
  - name: symbol
    type: string
    mandatory: true
    default: N/A
    description: symbol
    ranges:
  - name: size
    type: integer
    mandatory: false
    default: 20
    description: page size
    ranges:
  - name: fromId
    type: integer
    mandatory: false
    default: N/A
    description: 
    ranges:

content_markdown: |-
              #### **Note**

              For Market Makers Only

              #### **Limit Flow Rules**

              200/s/apikey
left_code_blocks:
  - code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
        "result": {
          "total": 7,
          "size": 7,
          "content": [
            { 
                    "orderId": "555841481206904320",   //Order id
                    "clientOrderId": "123",            //Client Order Id
                    "symbol": "btc_usdt",              //Trading pair
                    "state": "NEW",                    //Order State NEW,PLACED,PARTIALLY_FILLED
                    "contractSize": 0.000100000000,    //Contract size
                    "orderType": "LIMIT",              //Order type
                    "orderSide": "BUY",                //Order side
                    "positionSide": "LONG",            //Position side
                    "positionType": "CROSSED",         //Position type
                    "timeInForce": "GTC",              //Valid type
                    "price": "90000",                  //Order price
                    "origQty": "10000",                //Quantity (Cont)
                    "avgPrice": null,                  //Average Price
                    "executedQty": "0",                //Volume (Cont)
                    "marginFrozen": "4554",            //Occupied margin
                    "leverage": 20,                    //Leverage
                    "openPrice": null,
                    "closeProfit": "0",                
                    "createdTime": 1762224936156,
                    "updatedTime": 1762224936227,
                    "markPrice": "106524.9"            //Mark Price
            }
          ]
        },
        "returnCode": 0
      }
    title: Response
    language: json
---