---
title: 获取用户资金
position_number: 4
type: get
description: /az/future/user/v1/balance/list

content_markdown: |-

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
          "msgInfo": "success",
          "returnCode": 0,
          "result": [
            {
                "coin": "usdt",                         //币种
                "walletBalance": "5000019.09277742",    //钱包余额
                "openOrderMarginFrozen": "11.419247",   //订单冻结
                "isolatedMargin": "0",                  //逐仓保证金冻结
                "crossedMargin": "19.62351083",         //全仓起始保证金
                "availableBalance": "4999988.05001959", //可用余额
                "bonus": "0",                           //体验金余额
                "bonusDisRate": "0.5",                  //触发时的体验金抵扣率
                "coupon": "0"                           //抵扣金余额        
            }
          ]
        }
      title: Response
      language: json
---