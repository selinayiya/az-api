---
title: 根据id查询订单
position_number: 4
type: get
description: /az/future/trade/v1/order/detail
parameters:
  - name: orderId
    type: integer
    mandatory: true
    default: N/A
    description: 订单id
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
        "msgInfo": "success",
        "returnCode": 0,
        "result": {
            "orderId": "554854882113899648", //订单id
            "symbol": "btc_usdt",            //交易对
            "contractSize": 1.0E-4,          //合约面值
            "orderType": "LIMIT",            //订单类型
            "orderSide": "BUY",              //买卖方向
            "positionSide": "LONG",          //持仓方向
            "positionType": "CROSSED",       //仓位类型
            "timeInForce": "GTC",            //有效类型
            "closePosition": false,          //是否条件全平仓
            "price": "26972.9",              //委托价格
            "origQty": "4",                  //数量（张）
            "executedQty": "0",              //已成交数量（张）
            "marginFrozen": "0.539458",      //占用保证金
            "sourceType": "DEFAULT",         //来源类型
            "forceClose": false,             //是否是强平订单
            "leverage": 20,                  //下单时杠杠
            "state": "NEW",                  //订单状态 NEW：新建订单（未成交）；PARTIALLY_FILLED：部分成交；PARTIALLY_CANCELED：部分撤销；FILLED：全部成交；CANCELED：已撤销；REJECTED：下单失败；EXPIRED：已过期
            "createdTime": 1761989712601,    //创建时间
            "updatedTime": 1761989712656,    //更新时间
            "welfareAccount": false,         //是否体验金
            "markPrice": "110037.1",         //订单上的标记价格
            "profit": false                  //是否触发止盈止损订单
        }
      }
    title: Response
    language: json
---