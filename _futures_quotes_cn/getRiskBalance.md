---
title: 获取交易对风险基金余额
position_number: 20
type: get
description: /az/future/market/v1/public/contract/risk-balance
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 方向（PREV:上一页；NEXT:下一页）
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default: N/A
        description: id
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: 条数
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
                "hasPrev": false,                     //是否有上一页
                "hasNext": true,                      //是否有下一页
                "items": [
                    {
                        "id": "554744372432733187",   //id
                        "coin": "usdt",               //币种
                        "amount": "-10624.3177",      //余额
                        "createdTime": 1761963365040  //时间戳
                    }
                ]
          }
        }
      title: Response
      language: json
---