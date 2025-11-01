---
title: Best Price
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
    **request**

    format: best_price@\{symbol\}

    eg: best_price@btc\_usdt
    
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
                    "topic": "best_price", 
                    "event": "best_price@btc_usdt", 
                    "data": {
                        "s": "btc_usdt", //symbol
                        "a": "109598.4", //ask
                        "b": "109598.3", //bid
                        "t": 123124124   //timestamp
                    }
                }
        title: Response
        language: json
---
