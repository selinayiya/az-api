---
title: Get Trading Pair Information of Kline
position_number: 15
type: get
description: /az/future/market/v1/public/q/kline
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
    -
        name: interval
        type: string
        mandatory: true
        default: N/A
        description: Time-interval
        ranges: 1m;3m;5m;15m;30m;1h;2h;4h;6h;8h;12h;1d;2d;3d;1w;1M
    -
        name: startTime
        type: integer
        mandatory: false
        default: current time
        description: Start time
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: current time
        description: End time
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: 500
        description: Limit
        ranges:
content_markdown: Note：This method does not require a signature.
left_code_blocks:
    -
        code_block: "public void getKLine() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/v1/getKLine?market=btc_usdt&type=1min&since=0\");\r\n\tSystem.out.println(text);\r\n}"
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
                "s": "btc_usdt",    //Symbol
                "p": "btc_usdt",    //Trading pair
                "t": 1761981840000, //Timestamp
                "o": "110099.8",    //Open price
                "c": "110134.7",    //Close price
                "h": "110134.8",    //Highest price
                "l": "110089.3",    //Lowest price
                "a": "2998",        //Volume
                "v": "33010.77054"  //Turnover
            }
          ]
        }
      title: Response
      language: json
---