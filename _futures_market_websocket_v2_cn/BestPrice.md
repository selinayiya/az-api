---
title: 最优价格
position_number: 15
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

    语法: best_price@\{symbol\}

    示例: best_price@btc\_usdt
    
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
                    "topic": "best_price", 
                    "event": "best_price@btc_usdt", 
                    "data": {
                        "s": "btc_usdt", //交易对
                        "a": "109598.4", //卖出价
                        "aa": "2710",    //卖出数量
                        "b": "109598.3", //买入价
                        "ba": "3784",    //买入数量
                        "t": 123124124   //时间戳
                    }
                }
        title: Response
        language: json
---
