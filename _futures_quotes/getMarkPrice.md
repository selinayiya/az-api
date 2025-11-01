---
title: Get Mark Price for Single Trading Pair
position_number: 13
type: get
description: /az/future/market/v1/public/q/symbol-mark-price
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
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
          "result": {
                "s": "btc_usdt",   //Trading pair
                "p": "110069.5",   //Price
                "t": 1761981015615 //Timestamp
          }
        }
      title: Response
      language: json
---