---
title: Get the open position of a trading pair
position_number: 21
type: get
description: /az/future/market/v1/public/contract/open-interest
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
content_markdown: >-

  #### **Limit Flow Rules**

  1/s/ip
  <br>
  Note：This method does not require a signature.
  
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
                "symbol": "btc_usdt",               //Trading pair
                "openInterest": "222.6832",         //Open position
                "openInterestUsd": "24442143.06946",//Open value
                "time": 1761985665202               //Timestamp
          }
        }
      title: Response
      language: json
---