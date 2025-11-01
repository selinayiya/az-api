---
title: Balance change
position_number: 7
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
                 "{balance}@{listenKey}",
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
                "topic": "balance", 
                "event": "balance@123456", 
                "data": {
                          "coin": "usdt",                        //Currency
                          "underlyingType": 2,                   //1:Coin-M,2:USDT-M
                          "walletBalance": "9652.09217635",      // Balance
                          "openOrderMarginFrozen": "0.00000000", // Frozen order
                          "isolatedMargin": "0",                 // Isolated Margin
                          "crossedMargin": "38.58021896",        //Crossed Margin
                          "availableBalance": "9613.51195739",   //Available Balance
                          "coupon": "0",                         //Coupon
                          "bonus": "0"                           //Bonus
                   }  
            }
        title: Response
        language: json
---
