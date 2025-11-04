---
title: 获取用户资产信息（做市商）
position_number: 19
type: get
description: /az/future/cache/v1/balance
parameters:

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
          "msgInfo": "success",
          "returnCode": 0,
          "result": {
                    "coin": "usdt",                     //币种
                    "walletBalance": "996502.4870303",  //钱包余额
                    "openOrderMarginFrozen": "0",       //开仓占用保证金
                    "isolatedMargin": "0",
                    "crossedMargin": "10703.640957",    //全仓占用保证金
                    "availableBalance": "985798.8460733",  //可用余额
                    "openOrderFeeFrozen": "0"   
          }
        }
      title: Response
      language: json
---