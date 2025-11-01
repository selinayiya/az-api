---
title: K线
position_number: 9
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

    &nbsp;

    语法: kline@\{symbol\},\{interval\}

    interval: 1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1d, 3d, 1w, 1M

    示例: kline@btc\_usdt,5m
    
    速率: 1000ms

    &nbsp;
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                    "topic": "kline",
                    "event": "kline@btc_usdt,4h",
                    "data": {
                      "s": "btc_usdt",      //交易对
                      "o": "110096.3",      //open 开盘价
                      "c": "109933.6",      //cloes 收盘价
                      "h": "110164.4",      //high 最高价
                      "l": "109654.6",      //low 最低价
                      "a": "122187",        //amount 成交量
                      "v": "1344027.60259", //volume 成交额
                      "i": "4h",            //interval
                      "t": 1761998400000    //时间戳
                    }          
                }
        title: Response
        language: json
---
