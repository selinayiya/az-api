---
title: 余额变更
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
                            "coin": "usdt",                        //币种
                            "underlyingType": 2,                   //1:币本位，2:U本位
                            "walletBalance": "9652.09217635",      // 钱包余额
                            "openOrderMarginFrozen": "0.00000000", // 订单冻结
                            "isolatedMargin": "0",                 // 逐仓保证金
                            "crossedMargin": "38.58021896",        //全仓保证金
                            "availableBalance": "9613.51195739",   //可用余额
                            "coupon": "0",                         //抵扣金余额
                            "bonus": "0"                           //体验金余额
                   }  
            }
        title: Response
        language: json
---
