---
title: 获取交易对的k线信息
position_number: 15
type: get
description: /az/future/market/v1/public/q/kline
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: 交易对
        ranges:
    -
        name: interval
        type: string
        mandatory: true
        default: N/A
        description: 时间间隔
        ranges: 1m;3m;5m;15m;30m;1h;2h;4h;6h;8h;12h;1d;2d;3d;1w;1M
    -
        name: startTime
        type: integer
        mandatory: false
        default: 当前时间
        description: 起始时间
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: 当前时间
        description: 结束时间
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: 500
        description: 限制条数
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
                "s": "btc_usdt",    //交易对
                "p": "btc_usdt",    //交易对pair
                "t": 1761981840000, //时间戳
                "o": "110099.8",    //开始价
                "c": "110134.7",    //结束价
                "h": "110134.8",    //最高价
                "l": "110089.3",    //最低价
                "a": "2998",        //成交量
                "v": "33010.77054"  //成交额
            }
          ]
        }
      title: Response
      language: json
---