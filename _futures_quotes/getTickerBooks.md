---
title: Get Ask Bid Market Information for All Trading Pairs
position_number: 19
type: get
description: /az/future/market/v1/public/q/ticker/books
parameters:
content_markdown: Note：This method does not require a signature.
left_code_blocks:
    -
        code_block: "public void getTickerBokk() {\r\n\tString text = HttpUtil.get(URL + \"/data/api//az/future/market/v1/public/q/ticker/books?symbol=btc_usdt\");\r\n\tSystem.out.println(text);\r\n}"
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
                "s": "btc_usdt",    //Trading pair
                "t": 1761983754635, //Timestamp
                "ap": "110045.0",   //ask price
                "aq": "13619",      //ask amount
                "bp": "110044.9",   //bid price
                "bq": "9667"        //bid amount
            }
          ]
        }
      title: Response
      language: json
---