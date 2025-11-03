---
title: Change position
position_number: 8
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
           "{position}@{listenKey}",
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
                "topic": "position", 
                "event": "position@123456", 
                "data": {
                            "accountId": 8654006125462,
                            "accountType": 0,
                            "symbol": "btc_usdt",
                            "contractType": "PERPETUAL",    //PERPUTUAL，DELIVERY
                            "positionType": "CROSSED",      // "ISOLATED", "CROSSED"
                            "positionSide": "LONG",
                            "positionSize": "20",           // Position quantity
                            "closeOrderSize": "0",          //  Pending order quantity (Cont)
                            "availableCloseSize": "20",     //  Available quantity (Cont)
                            "realizedProfit": "-113.4475",  //  Realized profit and loss
                            "entryPrice": "107577.0",       //  Open position average price
                            "openOrderSize": "0",
                            "isolatedMargin": "21.59097358",  //  Isolated Margin
                            "openOrderMarginFrozen": "0.00000000",  //  Occupied open position margin
                            "underlyingType": "U_BASED",    // COIN_BASED, U_BASED
                            "leverage": 10,                 // Leverage
                            "welfareAccount": false,
                            "closeProfit": "232.7172",      //Closed Profit and Loss
                            "totalFee": "-133.1456",        //Total fee
                            "totalFundFee": "-213.0191",    //Total fund fee
                            "markPrice": "106208.1",
                            "profitFixedLatest": {},
                            "updatedTime": 1762184243057
                   }
            }
        title: Response
        language: json
---
