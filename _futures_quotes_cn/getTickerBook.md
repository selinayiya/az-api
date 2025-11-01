---
title: 获取指定交易对的买一卖一行情信息
position_number: 18
type: get
description: /az/future/market/v1/public/q/ticker/book
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
        code_block: "public void getTickerBokk() {\r\n\tString text = HttpUtil.get(URL + \"/data/api//az/future/market/v1/public/q/ticker/book?symbol=btc_usdt\");\r\n\tSystem.out.println(text);\r\n}"
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
                "s": "btc_usdt",    //交易对
                "t": 1761983754635, //时间戳
                "ap": "110045.0",   //卖一价格
                "aq": "13619",      //卖一数量
                "bp": "110044.9",   //买一价格
                "bq": "9667"        //买一数量
        }
      }
    title: Response
    language: json
---