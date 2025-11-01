---
title: Get Market Information for Specific Trading Pair
position_number: 7
type: get
description: /az/future/market/v1/public/q/ticker
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
                "t": 1761978054921,    //Timestamp
                "s": "btc_usdt",       //Trading pair
                "c": "109981.3",       //Latest price
                "h": "114308.1",       //Highest price in 24 hours
                "l": "108600.0",       //Lowest price in 24 hours
                "a": "3128038",        //24h volume
                "v": "34412784.72516", //24h turnover
                "o": "109658.1",       //The first transaction price 24 hours ago
                "r": "0.0029"          //24h Price Fluctuation Limit
          }
        }
      title: Response
      language: json
---