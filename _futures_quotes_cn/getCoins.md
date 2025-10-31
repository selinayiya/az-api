---
title: 获取交易对币种
position_number: 2
type: get
description: /az/future/market/v1/public/symbol/coins

parameters:
  - name:
    content:
content_markdown: 注：**此方法不需要签名**
left_code_blocks:
  - code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/market/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
        "returnCode": 0
        "result": [
            "usdt"
         ],
      }
    title: Response
    language: json
---