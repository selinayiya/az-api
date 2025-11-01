---
title: See Leverage Stratification of All Trading Pairs
position_number: 6
type: get
description: /az/future/market/v1/public/leverage/bracket/list
parameters:
content_markdown: Note：This method does not require a signature.
left_code_blocks:
    -
        code_block: "public void getKLine() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/market/v1/getKLine?market=btc_usdt&type=1min&since=0\");\r\n\tSystem.out.println(text);\r\n}"
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
              "symbol": "eth_usdt",
              "leverageBrackets": [
                {
                    "symbol": "eth_usdt",       //Trading pair
                    "bracket": 1,               //Level
                    "maxNominalValue": "50000", //Maximum notional value
                    "maintMarginRate": "0.004", //Maintain margin rate
                    "startMarginRate": "0.005", //Initial margin rate
                    "maxLeverage": "125",       //Maximum leverage
                    "minLeverage": "1"          //Minimum leverage
                }
              ]
            }
          ]
        }
      title: Response
      language: json
---