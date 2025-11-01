---
title: Get Depth Data of Trading Pairs
position_number: 10
type: get
description: /az/future/market/v1/public/q/depth
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
    -
        name: level
        type: integer
        mandatory: true
        default: N/A
        description: "Level(min:1,max:50)\t"
        ranges:
content_markdown: >-

  #### **Limit Flow Rules**

  10/s/ip
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
                "t": 1761979495332,  //Timestamp
                "s": "btc_usdt",     //Trading pair
                "u": 1761965792147,  //updateId
                "b": [               //BID
                    [
                        "109923.4",
                        "18679"
                    ]
                ],
                "a": [               //ASK
                    [
                        "109923.5",
                        "1773"
                    ]
                ]        
          }
        }
      title: Response
      language: json
---