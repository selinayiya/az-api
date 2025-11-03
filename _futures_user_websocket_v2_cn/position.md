---
title: 仓位变更
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
                            "accountId": 8654006125462,    //账号id
                            "accountType": 0,              //账号类型
                            "symbol": "btc_usdt",          //交易对
                            "contractType": "PERPETUAL",   //合约类型，PERPUTUAL，DELIVERY
                            "positionType": "CROSSED",     // "ISOLATED", "CROSSED"
                            "positionSide": "LONG",        //仓位方向：0单向持仓，正数为多仓，负数为空仓、1多、2空
                            "positionSize": "20",          //持仓数量
                            "closeOrderSize": "0",         //平仓挂单数量
                            "availableCloseSize": "20",    //可平仓张数
                            "realizedProfit": "-113.4475", //已实现盈亏
                            "entryPrice": "107577.0",      //开仓均价
                            "openOrderSize": "0",          //开仓订单占用
                            "isolatedMargin": "21.59097358", //逐仓保证金
                            "openOrderMarginFrozen": "0.00000000", //开仓订单占用保证金
                            "underlyingType": "U_BASED",    // COIN_BASED, U_BASED
                            "leverage": 10,                //杠杆倍数
                            "welfareAccount": false,
                            "closeProfit": "232.7172",     //平仓盈亏
                            "totalFee": "-133.1456",       //手续费
                            "totalFundFee": "-213.0191",   //资金费率
                            "markPrice": "106208.1",
                            "profitFixedLatest": {},
                            "updatedTime": 1762184243057    
                   }
            }
        title: Response
        language: json
---
