---
title: 获取单个交易对的最优价格
position_number: 14
type: get
description: /az/future/market/v1/public/q/best-price
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: 交易对
        ranges:
content_markdown: 注：**此方法不需要签名**
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
                "symbol": "btc_usdt",  //交易对
                "ask": "109598.4",     //卖出价
                "bid": "109598.3",     //买入价
                "time": 1761965026050  //时间戳
             }
        }
      title: Response
      language: json
---