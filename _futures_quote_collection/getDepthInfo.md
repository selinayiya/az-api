---
title: Get Depth Info
position_number: 2
type: get
description: /az/future/market/v1/public/cg/orderbook
remark: Content-Type = application/x-www-form-urlencoded
parameters:
  -
    name: symbol
    type: string
    mandatory: true
    default: N/A
    description: Trading pair, eg.BTC-USDT
    ranges:
  -
    name: level
    type: int
    mandatory: false
    default: 50
    description:
    ranges: 1-200
        
content_markdown: Note：This method does not require a signature.
left_code_blocks:
  - code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/market/v1/public/cg/orderbook\");\r\n\tSystem.out.println(text);\r\n}"
    title: Java
    language: java
right_code_blocks:
  - code_block: |-
      {
            "ticker_id": "BTC-USDT",
            "timestamp": 1761987036772,
            "bids": [
              [
                "110166.2",
                "16515"
              ]
            ],
            "asks": [
              [
                "110166.3",
                "7092"
              ]
            ]
      }
    title: Response
    language: json
---