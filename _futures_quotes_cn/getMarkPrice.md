---
title: 获取单个交易对的标记价格
position_number: 13
type: get
description: /az/future/market/v1/public/q/symbol-mark-price
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
                "s": "btc_usdt",   //交易对
                "p": "110069.5",   //价格
                "t": 1761981015615 //时间
          }
        }
      title: Response
      language: json
---