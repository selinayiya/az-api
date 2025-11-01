---
title: 查询历史订单
position_number: 1.1
type: get
description: /az/future/trade/v1/order/list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: 交易对
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "方向（PREV:上一页；NEXT:下一页）\t"
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default: N/A
        description: id
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: 10
        description: "条数\t"
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default: N/A
        description: 起始时间
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default: N/A
        description: 结束时间
        ranges:
content_markdown: |-

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
          "hasNext": false,                     //是否有下一页
          "hasPrev": false,                     //是否有上一页
          "items": [ 
            {
                "orderId": "554845056780618880", //订单id
                "symbol": "btc_usdt",        //交易对
                "contractSize": 1.0E-4,      //合约面值
                "orderType": "LIMIT",        //订单类型
                "orderSide": "BUY",          //买卖方向
                "positionSide": "LONG",      //持仓方向
                "positionType": "CROSSED",   //仓位类型
                "timeInForce": "GTC",        //有效类型
                "closePosition": false,      //是否条件全平仓
                "price": "26972.9",          //委托价格
                "origQty": "4",              //数量（张）
                "executedQty": "0",          //已成交数量（张）
                "marginFrozen": "0.539458",  //占用保证金
                "sourceType": "DEFAULT",     //来源类型
                "forceClose": false,         //是否是强平订单
                "leverage": 20,
                "state": "NEW",              //订单状态 NEW：新建订单（未成交）；PARTIALLY_FILLED：部分成交；PARTIALLY_CANCELED：部分撤销；FILLED：全部成交；CANCELED：已撤销；REJECTED：下单失败；EXPIRED：已过期
                "createdTime": 1761987370059,//创建时间
                "updatedTime": 1761987370106,
                "welfareAccount": false,     //是否体验金
                "markPrice": "110181.6",     //订单上的标记价格
                "profit": false              //是否触发止盈止损订单
            }
          ]
        },
        "returnCode": 0
      }
    title: Response
    language: json
---