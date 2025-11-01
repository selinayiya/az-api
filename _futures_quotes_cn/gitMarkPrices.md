---
title: 获取所有交易对的标记价格
position_number: 14
type: get
description: /az/future/market/v1/public/q/mark-price
parameters:
    -
        name: symbol
        type: string
        mandatory: false
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
          "result": [
            {
                "s": "btc_usdt",   //交易对
                "p": "110099.3",   //价格
                "t": 1761981389615 //时间戳
            }
          ]
        }
      title: Response
      language: json
---