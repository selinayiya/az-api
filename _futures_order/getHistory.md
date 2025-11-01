---
title: See Order History
position_number: 1.1
type: get
description: /az/future/trade/v1/order/list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: "Trading pairs (queries all trading pairs if not passed)\t"
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "Direction（PREV:Previous page；NEXT:Next page）\t"
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default: N/A
        description: id
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: "Limit\t"
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default: N/A
        description: Start time
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: N/A
        description: End time
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
        "msgInfo": "",
        "result": {
          "hasNext": false,                     //Is there a next page
          "hasPrev": false,                     //Is there a previous page
          "items": [ 
            {
                "orderId": "554845056780618880", //Order ID
                "symbol": "btc_usdt",        //Trading pair
                "contractSize": 1.0E-4,      //Contract size
                "orderType": "LIMIT",        //Order type
                "orderSide": "BUY",          //Order side
                "positionSide": "LONG",      //Position side
                "positionType": "CROSSED",   //Position type
                "timeInForce": "GTC",        //Valid type
                "closePosition": false,      //Whether to close all when order condition is triggered
                "price": "26972.9",          //Order price
                "origQty": "4",              //Quantity (Cont)
                "executedQty": "0",          //Volume (Cont)
                "marginFrozen": "0.539458",  //Occupied margin
                "sourceType": "DEFAULT",     //Source type
                "forceClose": false,         //Is it a liquidation order
                "leverage": 20,
                "state": "NEW",              //Order state:NEW：New order (unfilled);PARTIALLY_FILLED:Partial deal;PARTIALLY_CANCELED:Partial revocation;FILLED:Filled;CANCELED:Cancled;REJECTED:Order failed;EXPIRED：Expired
                "createdTime": 1761987370059,//Creat time
                "updatedTime": 1761987370106,
                "welfareAccount": false,     //Is Experience Fund
                "markPrice": "110181.6",     //Mark Price
                "profit": false              //Is Take-Profit/Stop-Loss Order Triggered
            }
          ]
        },
        "returnCode": 0
      }
    title: Response
    language: json
---