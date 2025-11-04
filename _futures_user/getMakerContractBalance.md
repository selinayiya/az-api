---
title: Get User's Fund Information (Maker)
position_number: 19
type: get
description: /az/future/cache/v1/balance
parameters:

content_markdown: |-
              #### **Note**

              For Market Makers Only

              #### **Limit Flow Rules**

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
                "coin": "usdt",                     //Currency
                "walletBalance": "996502.4870303",  //Balance
                "openOrderMarginFrozen": "0",       //Frozen order
                "isolatedMargin": "0",              //Frozen isolated margin
                "crossedMargin": "10703.640957",    //Crossed Margin
                "availableBalance": "985798.8460733",  //Available balance
                "openOrderFeeFrozen": "0"        
          }
        }
      title: Response
      language: json
---