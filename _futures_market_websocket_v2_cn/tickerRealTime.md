---
title: ticker
position_number: 10
type:
description: 

parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **请求**

    语法: ticker@\{symbol\}

    示例: ticker@btc\_usdt
    
    速率: 1000ms
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "topic": "ticker",
                    "event": "ticker@btc_usdt",
                    "data": {
                      "s": "btc_usdt",      //交易对
                      "o": "109927.8",      // open 开盘价
                      "c": "109822.7",      //cloes 收盘价
                      "h": "114308.1",      //high 最高价
                      "l": "108600.0",      //low 最低价
                      "a": "1877436",       //amount 成交量
                      "v": "20640737.33039",//volume 成交额
                      "r": "-0.0009",       //24小时涨跌幅
                      "t": 1762007085988    //时间戳
                    }
                }
        title: Response
        language: json
---
