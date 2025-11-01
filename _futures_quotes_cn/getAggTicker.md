---
title: 获取指定交易对的聚合行情信息
position_number: 16
type: get
description: /az/future/market/v1/public/q/agg-ticker
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
                "t": 1761982678496,         //时间戳
                "s": "btc_usdt",            //交易对
                "c": "110163.8",            //最新价
                "h": "114308.1",            //24小时最高价
                "l": "108600.0",            //24小时最低价
                "a": "3140672",             //24小时成交量
                "v": "34554966.27918",      //24小时成交额
                "o": "109469.0",            //24小时前第一笔成交价
                "r": "0.0063",              //24小时涨跌幅
                "i": "110201.470933300000", //指数价格
                "m": "110163.8",            //标记价格
                "bp": "110163.7",           //买一价格
                "ap": "110163.8"            //卖一价格
        }
      }
    title: Response
    language: json
---