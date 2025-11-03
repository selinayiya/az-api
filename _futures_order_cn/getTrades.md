---
title: 查询成交明细
position_number: 1.1
type: get
description: /az/future/trade/v1/order/trade-list
parameters:
    -
        name: orderId
        type: integer
        mandatory: false
        default: N/A
        description: 订单id
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default: N/A
        description: 交易对
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
    -
        name: fromId
        type: string
        mandatory: false
        default:
        description: 上次开始分页的Id，即记录的主键id
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 分页方向
        ranges: NEXT：下一页，PREV：上一页
    -
        name: size
        type: int
        mandatory: false
        default: 10
        description: 每页记录数，最大不超过100
        ranges: 1<=limit<=100
content_markdown: |-

               #### **限流规则**

               200/s/apikey
left_code_blocks:
    -
        code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/trade/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
                "hasPrev": false,
                "hasNext": false,
                "items": [
                    {
                        "id": "123",                     //Id
                        "orderId": "551497070209712960", //订单id
                        "execId": "551497070368784451",  //成交id
                        "symbol": "btc_usdt",            //交易对
                        "contractSize": 1.0E-4,          //合约面值
                        "quantity": "4",                 //成交数量
                        "price": "108460.5",             //成交价格
                        "fee": "0.02603052",             //手续费
                        "feeCoin": "usdt",               //手续费币种
                        "timestamp": 1761189147896,      //时间戳
                        "takerMaker": "TAKER",           
                        "orderSide": "BUY",              //买卖方向
                        "positionSide": "LONG"           //持仓方向
                    }
                ]
          }
        }
      title: Response
      language: json
---