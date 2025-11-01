---
title: Ticker
position_number: 11
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

    format: ticker@\{symbol\}

    eg: ticker@btc\_usdt
    
    rate: 1000ms
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
                        "s": "btc_usdt",      //trading pair
                        "o": "109927.8",      // opening price
                        "c": "109822.7",      //Closing price
                        "h": "114308.1",      //highest price
                        "l": "108600.0",      //low 最低价
                        "a": "1877436",       //volume
                        "v": "20640737.33039",//Turnover
                        "r": "-0.0009",       //24-hour Price Change Percentage
                        "t": 1762007085988    //timestamp
                      }
                }
        title: Response
        language: json
---
