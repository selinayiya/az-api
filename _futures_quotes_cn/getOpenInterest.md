---
title: 获取交易对开仓量
position_number: 21
type: get
description: /az/future/market/v1/public/contract/open-interest
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: 交易对
        ranges:
content_markdown: >-

  #### **限流规则**

  1/s/ip
  <br>
  注：此方法不需要签名
  
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
                "symbol": "btc_usdt",               //交易对
                "openInterest": "222.6832",         //开仓量
                "openInterestUsd": "24442143.06946",//开仓价值
                "time": 1761985665202               //时间戳
          }
        }
      title: Response
      language: json
---