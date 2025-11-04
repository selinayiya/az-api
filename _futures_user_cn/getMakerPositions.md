---
title: 获取持仓信息（做市商）
position_number: 20
type: get
description: /az/future/cache/v1/positions
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: 交易对（不传时查询所有交易对的持仓信息）
        ranges:
content_markdown: |-
              #### **备注**

              仅供做市商使用

              #### **限流规则**

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
                "symbol": "btc_usdt",        //交易对
                "positionType": "CROSSED",   //持仓模式
                "positionSide": "LONG",      //持仓方向
                "leverage": 20,              //杠杆倍数
                "positionSize": "7000",      //持仓头寸数量(张)
                "closeOrderSize": "0",
                "availableCloseSize": "7000",  //可平仓数量(张)
                "entryPrice": "110000",        //开仓均价
                "openOrderSize": "0", 
                "isolatedMargin": "3850",      //持仓占用保证金
                "openOrderMarginFrozen": "0",
                "realizedProfit": "880.05305855",  //已实现盈亏
                "closeProfit": "0",
                "totalFee": "-77.846426",
                "totalFundFee": "5857.22457151",   //已收取资金费率
                "contractSize": "0.0001",
                "markPrice": "106896.5",           //最新标记价格
                "updatedTime": "1762221600282"
            }
          ],
          "returnCode": 0
        }
      title: Response
      language: json
---
