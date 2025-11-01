---
title: Get Funding Rate Records
position_number: 19
type: get
description: /az/future/market/v1/public/q/funding-rate-record
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: Trading pair
        ranges:
    -
        name: id
        type: integer
        mandatory: false
        default: N/A
        description: id
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "Direction（PREV:Previous page；NEXT:Next page）\t"
        ranges: PREV;NEXT
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: "Limit\t"
        ranges:
content_markdown: Note：This method does not require a signature.
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
                "hasPrev": false,                        //Is there a previous page
                "hasNext": true,                         //Is there a next page
                "items": [
                    {
                        "id": "554830922718404672",      //id
                        "symbol": "btc_usdt",            //Trading pair
                        "fundingRate": "-0.000162821857",//Latest funding rate
                        "createdTime": 1761984000000,    //Create Timestamp
                        "collectionInternal": 3600       //Billing Cycle (second)
                    }
                ]
          }
        }
      title: Response
      language: json
---