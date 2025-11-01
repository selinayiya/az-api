---
title: Get User's Funds Information
position_number: 4
type: get
description: /az/future/user/v1/balance/list
content_markdown: |-

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
          "result": [
            {
                "coin": "usdt",                         //Currency
                "walletBalance": "5000019.09277742",    //Balance
                "openOrderMarginFrozen": "11.419247",   //Frozen order
                "isolatedMargin": "0",                  //Frozen isolated margin
                "crossedMargin": "19.62351083",         //Crossed Margin
                "availableBalance": "4999988.05001959", //Available balance
                "bonus": "0",                           //Bouns
                "bonusDisRate": "0.5",                  //Experience Fund Deduction Rate at Trigger
                "coupon": "0"                           //Coupon        
            }
          ]
        }
      title: Response
      language: json
---