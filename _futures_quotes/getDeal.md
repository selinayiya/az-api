---
title: Get Latest Transaction Information of Trading Pairs
position_number: 9
type: get
description: /az/future/market/v1/public/q/deal
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
    -
        name: num
        type: integer
        mandatory: false
        default: 50
        description: Quantity
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
          "result": [
            {
                "t": 1761978847393, //Timestamp
                "s": "btc_usdt",    //Trading pair
                "p": "110088.8",    //Price
                "a": "3",           //Volume
                "m": "BID"          //Order side
            }
          ]
        }
      title: Response
      language: json
---