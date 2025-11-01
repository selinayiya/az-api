---
title: 获取资金费率记录
position_number: 19
type: get
description: /az/future/market/v1/public/q/funding-rate-record
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: 交易对
        ranges:
    -
        name: id
        type: integer
        mandatory: false
        default: N/A
        description: id
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "方向（PREV:上一页；NEXT:下一页）\t"
        ranges: PREV;NEXT
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: "条数\t"
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
                "hasPrev": false,                        //是否有上一页
                "hasNext": true,                         //是否有下一页
                "items": [
                    {
                        "id": "554830922718404672",      //id
                        "symbol": "btc_usdt",            //交易对
                        "fundingRate": "-0.000162821857",//最新资金费率
                        "createdTime": 1761984000000,    //时间戳
                        "collectionInternal": 3600       //收取时间间隔（秒）
                    }
                ]
          }
        }
      title: Response
      language: json
---