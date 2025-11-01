---
title: See Orders by ID
position_number: 4
type: get
description: /az/future/trade/v1/order/detail
parameters:
  - name: orderId
    type: integer
    mandatory: true
    default: N/A
    description: Order ID
    ranges:
content_markdown: |-

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
        "msgInfo": "success",
        "returnCode": 0,
        "result": {
            "orderId": "554854882113899648", //Order id
            "symbol": "btc_usdt",            //Trading pair
            "contractSize": 1.0E-4,          //Contract size
            "orderType": "LIMIT",            //Order type
            "orderSide": "BUY",              //Order side
            "positionSide": "LONG",          //Position side
            "positionType": "CROSSED",       //Position type
            "timeInForce": "GTC",            //Valid type
            "closePosition": false,          //Whether to close all when order condition is triggered
            "price": "26972.9",              //Order price
            "origQty": "4",                  //Quantity (Cont)
            "executedQty": "0",              //Volume (Cont)
            "marginFrozen": "0.539458",      //Occupied margin
            "sourceType": "DEFAULT",         //Source type
            "forceClose": false,             //Is it a liquidation order
            "leverage": 20,                  //Leverage
            "state": "NEW",                  //Order state:NEW：New order (unfilled);PARTIALLY_FILLED:Partial deal;PARTIALLY_CANCELED:Partial revocation;FILLED:Filled;CANCELED:Cancled;REJECTED:Order failed;EXPIRED：Expired
            "createdTime": 1761989712601,    //Create time
            "updatedTime": 1761989712656,    //Update time
            "welfareAccount": false,         //Is Trial Fund
            "markPrice": "110037.1",         //Mark Price
            "profit": false                  //Is Take-Profit/Stop-Loss Order Triggered
        }
      }
    title: Response
    language: json
---