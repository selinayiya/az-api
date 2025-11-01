---
title: 查询单个交易对杠杆分层
position_number: 5
type: get
description: /az/future/market/v1/public/leverage/bracket/detail
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
            "symbol": "btc_usdt",
            "leverageBrackets": [
                  {
                    "symbol": "btc_usdt",       //交易对
                    "bracket": 1,               //档位
                    "maxNominalValue": "50000", //该层最大名义价值
                    "maintMarginRate": "0.004", //维持保证金率
                    "startMarginRate": "0.008", //起始保证金率
                    "maxLeverage": "125",       //最大杠杆倍数
                    "minLeverage": "1"          //最小杠杆倍数
                  }
            ]
          }
        }
      title: Response
      language: json
---