---
title: Get Best Price for Single Trading Pair
position_number: 14
type: get
description: /az/future/market/v1/public/q/best-price
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
        code_block: "public void getBestPrice() {\r\n\tString text = HttpUtil.get(URL + \"/az/future/market/v1/public/q/best-price?symbol=btc_usdt\");\r\n\tSystem.out.println(text);\r\n}"
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
                "symbol": "btc_usdt",  //Trading pair
                "ask": "109598.4",     //ASK
                "bid": "109598.3",     //BID
                "time": 1761965026050  //Timestamp
             }
        }
      title: Response
      language: json
---