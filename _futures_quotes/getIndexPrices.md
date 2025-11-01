---
title: Get Index Price for All Trading Pairs
position_number: 12
type: get
description: /az/future/market/v1/public/q/index-price
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
                "s": "eth_usdt",   //Trading pair
                "p": "3857.579503",//Price
                "t": 1761980457446 //Timestamp
            }
          ]
        }
      title: Response
      language: json
---