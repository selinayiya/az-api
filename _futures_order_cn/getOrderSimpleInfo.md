---
title: 根据订单id查询用户信息
position_number: 5
type: get
description: /az/future/trade/v1/order/slim
parameters:
  - name: orderId
    type: Long
    mandatory: true
    default: N/A
    description: 订单ID
    ranges:
      
content_markdown: |-
               #### **备注**
  
               仅供做市商使用

               #### **限流规则**

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
              "orderId": 17248809452176384,              //订单ID
              "orderClientIp": "127.0.0.1",              //下单用户IP
              "userWalletAddress": "0xDd3356f03xxxxx",   //下单用户钱包地址
              "chainType": "ETHEREUM"                    //链类型
        }
      }
    title: Response
    language: json
---