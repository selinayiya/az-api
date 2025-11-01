---
title: Get Aggregated Market Information for All Trading Pairs
position_number: 17
type: get
description: /az/future/market/v1/public/q/agg-tickers
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
                "t": 1761982678496,         //Timestamp
                "s": "btc_usdt",            //Trading pair
                "c": "110163.8",            //Latest price
                "h": "114308.1",            //Highest price in 24 hours
                "l": "108600.0",            //Lowest price in 24 hours
                "a": "3140672",             //24h volume
                "v": "34554966.27918",      //24h Turnover
                "o": "109469.0",            //The first transaction price 24 hours ago
                "r": "0.0063",              //24h price fluctuation limit
                "i": "110201.470933300000", //index price
                "m": "110163.8",            //mark price
                "bp": "110163.7",           //bid price
                "ap": "110163.8"            //ask price
            }
          ]
        }
      title: Response
      language: json
---