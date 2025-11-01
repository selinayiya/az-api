---
title: K-line
position_number: 8
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
    **request**

    &nbsp;

    format: kline@\{symbol\},\{interval\}

    interval: 1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1d, 3d, 1w, 1M

    eg: kline@btc\_usdt,5m
    
    rate: 1000ms

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
                        "s": "btc_usdt",      //trading pair
                        "o": "110096.3",      // opening price
                        "c": "109933.6",      //Closing price
                        "h": "110164.4",      //highest price
                        "l": "109654.6",      //lowest price
                        "a": "122187",        //volume
                        "v": "1344027.60259", //Turnover
                        "i": "4h",            //Interval
                        "t": 1761998400000    //Timestamp
                      }     
                }
        title: Response
        language: json
---
