---
title: See Transaction Details
position_number: 1.1
type: get
description: /az/future/trade/v1/order/trade-list
parameters:
    -
        name: orderId
        type: integer
        mandatory: false
        default: N/A
        description: Order ID
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: Trading pair
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default: N/A
        description: start time
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: N/A
        description: end time
        ranges:
    -
        name: fromId
        type: string
        mandatory: false
        default:
        description: Start ID, e.g. 6216559590087220004
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: query direction
        ranges: query direction:PREV, NEXT
    -
        name: size
        type: int
        mandatory: false
        default: 10
        description: Limit number, max 100
        ranges: 1<=limit<=100
content_markdown: |-

             #### **Limit Flow Rules**

             200/s/apikey
left_code_blocks:
    -
        code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
                "hasPrev": false,
                "hasNext": false,
                "items": [
                    {
                        "id": "123",                     //Id
                        "orderId": "551497070209712960", //Order Id
                        "execId": "551497070368784451",  //Execution Id
                        "symbol": "btc_usdt",            //Symbol
                        "contractSize": 1.0E-4,          //Contract Size
                        "quantity": "4",                 //Volume
                        "price": "108460.5",             //Price
                        "fee": "0.02603052",             //Fee
                        "feeCoin": "usdt",               //Currency of fee
                        "timestamp": 1761189147896,      //Timestamp
                        "takerMaker": "TAKER",           
                        "orderSide": "BUY",              //Order Size
                        "positionSide": "LONG",          //Position Size
                        "oppositeUserId": "372676",      //Opposite User Id
                        "oppositeOrderId": "55149707"    //Opposite Order Id
                    }
                ]
          }
        }
      title: Response
      language: json
---