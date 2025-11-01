---
title: Get Funding Rate Information
position_number: 18
type: get
description: /az/future/market/v1/public/q/funding-rate
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
                "symbol": "btc_usdt",               //Trading Pair
                "fundingRate": -1.53695081E-4,      //Latest Funding Rate
                "nextCollectionTime": 1761984000000,//Next Billing Date
                "collectionInternal": 1             //Billing Cycle (hour)
          }
        }
      title: Response
      language: json
---