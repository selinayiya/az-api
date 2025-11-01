---
title: 获取所有交易对的指数价格
position_number: 12
type: get
description: /az/future/market/v1/public/q/index-price
parameters:
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
                "s": "eth_usdt",   //交易对
                "p": "3857.579503",//价格
                "t": 1761980457446 //时间
            }
          ]
        }
      title: Response
      language: json
---