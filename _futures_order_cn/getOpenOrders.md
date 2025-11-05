---
title: 查询未完成订单（做市商）
position_number: 9
type: get
description: /az/future/cache/v1/open-orders
parameters:
  - name: symbol
    type: string
    mandatory: true
    default: N/A
    description: 交易对
    ranges:
  - name: size
    type: integer
    mandatory: false
    default: 20
    description: 单页数
    ranges:
  - name: fromId
    type: integer
    mandatory: false
    default: N/A
    description: 分页fromId，默认排序按照 orderId
    ranges:

content_markdown: |-
              #### **备注**

              仅供做市商使用

              #### **限流规则**

              200/s/apikey
left_code_blocks:
  - code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
    title: Java
    language: java
right_code_blocks:
  - code_block: |-
      {
        "error": {
          "code": "",
          "msg": ""
        },
        "msgInfo": "",
        "result": {
          "total": 7,
          "size": 7,
          "content": [
            { 
                    "orderId": "555841481206904320",   //订单id
                    "clientOrderId": "123",            //自定义id
                    "symbol": "btc_usdt",              //交易对
                    "state": "NEW",                    //订单状态 NEW,PLACED,PARTIALLY_FILLED
                    "contractSize": 0.000100000000,    //合约面值
                    "orderType": "LIMIT",              //订单类型
                    "orderSide": "BUY",                //买卖方向
                    "positionSide": "LONG",            //持仓方向
                    "positionType": "CROSSED",         //仓位类型
                    "timeInForce": "GTC",              //有效类型
                    "price": "90000",                  //委托价格
                    "origQty": "10000",                //数量（张）
                    "avgPrice": null,                  //平均价格
                    "executedQty": "0",                //已成交数量（张）
                    "marginFrozen": "4554",            //占用保证金
                    "leverage": 20,                    //下单时杠杠
                    "openPrice": null,
                    "closeProfit": "0",                //已实现盈亏
                    "createdTime": 1762224936156,
                    "updatedTime": 1762224936227,
                    "markPrice": "106524.9"            //订单上的标记价格
            }
          ],
          "page": 0,
          "ps": 0,
          "total": 0
        },
        "returnCode": 0
      }
    title: Response
    language: json
---