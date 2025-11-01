---
title: 获取指定交易对的行情信息
position_number: 7
type: get
description: /az/future/market/v1/public/q/ticker
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
                "t": 1761978054921,    //时间
                "s": "btc_usdt",       //交易对
                "c": "109981.3",       //最新价
                "h": "114308.1",       //24小时最高价
                "l": "108600.0",       //24小时最低价
                "a": "3128038",        //24小时成交量
                "v": "34412784.72516", //24小时成交额
                "o": "109658.1",       //24小时前第一笔成交价
                "r": "0.0029"          //24小时涨跌幅
          }
        }
      title: Response
      language: json
---