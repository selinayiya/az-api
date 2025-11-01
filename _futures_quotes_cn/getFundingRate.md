---
title: 获取资金费率
position_number: 18
type: get
description: /az/future/market/v1/public/q/funding-rate
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
                "fundingRate": -1.53695081E-4,      //最新资金费率
                "nextCollectionTime": 1761984000000,//下次收取时间
                "collectionInternal": 1             //收取时间间隔（时）
          }
        }
      title: Response
      language: json
---