---
title: Transactions
position_number: 9
type:
description: 

parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
  subscribe:
  ```js
    {
       "method": "SUBSCRIBE/UNSUBSCRIBE",
       "params": [
           "{trade}@{listenKey}",
        ],
       "id": "{id}"
    }
  ```

left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trade", 
                "event": "trade@123456", 
                "data": {
                        "id": "556931318219666113",
                        "orderId":"12312312",       // Order ID
                        "clientOrderId":"123456",   // Client order ID
                        "price":"34244",            // Price
                        "quantity":"123",           // Quantity
                        "marginUnfrozen":"123",     // Quantity of unfrozen margin
                        "timestamp":1731231231,     // Timestamp
                        "symbol": "btc_usdt",       //Symbol
                        "orderSide": "BUY",         //Order side
                        "positionSide": "LONG",     //Position side
                        "isMaker": true,            //Is maker or not, true:maker;false:taker
                        "fee": 0.0002,              //fee
                        "execId": "123",            //Execution id
                        "oppositeUserId": "1234",     //Opposite User Id, Provided for Market Makers Only
                        "oppositeOrderId": "2345"     //Opposite Order Id, Provided for Market Makers Only
                   }
            }
        title: Response
        language: json
---
