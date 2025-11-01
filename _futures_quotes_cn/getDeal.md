---
title: 获取交易对的最新成交信息
position_number: 9
type: get
description: /az/future/market/v1/public/q/deal
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: 交易对
        ranges:
    -
        name: num
        type: integer
        mandatory: false
        default: 50
        description: 数量
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
                "t": 1761978847393, //成交时间
                "s": "btc_usdt",    //交易对
                "p": "110088.8",    //成交价
                "a": "3",           //成交量
                "m": "BID"          //买卖方向
            }
          ]
        }
      title: Response
      language: json
---