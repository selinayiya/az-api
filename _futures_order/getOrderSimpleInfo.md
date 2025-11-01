---
title: See User Info by Order ID
position_number: 5
type: get
description: /az/future/trade/v1/order/slim
parameters:
  - name: orderId
    type: Long
    mandatory: true
    default: N/A
    description: Order Id
    ranges:
      
content_markdown: |-
               #### **Note**

               For Market Makers Only

               #### **Limit Flow Rules**

               200/s/apikey
left_code_blocks:
  - code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/az/future/trade/v1/order/slim\");\r\n\tSystem.out.println(text);\r\n}"
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
              "orderId": 17248809452176384,              //Order Id
              "orderClientIp": "127.0.0.1",              //Order Placing User IP
              "userWalletAddress": "0xDd3356f03xxxxx",   //Order Placing User Address
              "chainType": "ETHEREUM"                    //Chain Type
        }
      }
    title: Response
    language: json
---