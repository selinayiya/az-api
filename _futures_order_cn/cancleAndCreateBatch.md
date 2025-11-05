---
title: 批量下、撤单
position_number: 8
type: post
description: /az/future/trade/v1/order/batch
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
  - name: createOrderFirst
    type: bool
    mandatory: false
    default: true
    description: 默认下单优先，否则撤单优先
    ranges:
  - name: createOrders
    type: Set&lt;OrderCreateDTO&gt;
    mandatory: false
    default: 
    description: 下单列表，下单参数OrderCreateDTO集合
    ranges: 最大支持100个
  - name: cancelOrderIds
    type: Set&lt;Long&gt;
    mandatory: false
    default:
    description: 撤单列表，订单Id的集合
    ranges: 最大支持100个
      
tables:
  - title: OrderCreateDTO
    data:
      -
        name: clientOrderId
        type: string
        mandatory: true
        default: N/A
        description: 自定义订单id
        ranges:
      -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
      -
        name: orderSide
        type: string
        mandatory: true
        default: N/A
        description: 买卖方向：BUY;SELL
        ranges: BUY;SELL
      -
        name: orderType
        type: string
        mandatory: true
        default: N/A
        description: 订单类型：LIMIT；MARKET
        ranges: LIMIT；MARKET
      -
        name: origQty
        type: number
        mandatory: true
        default: N/A
        description: 数量（张）
        ranges:
      -
        name: price
        type: number
        mandatory: false
        default: N/A
        description: 价格
        ranges:
      -
        name: timeInForce
        type: string
        mandatory: false
        default: GTC
        description: 有效方式：GTC;IOC;FOK;GTX
        ranges: GTC;IOC;FOK;GTX
      -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default: N/A
        description: 止盈价
        ranges:
      -
        name: triggerStopPrice
        type: number
        mandatory: false
        default: N/A
        description: 止损价
        ranges:
      -
        name: positionSide
        type: string
        mandatory: true
        default: N/A
        description: 仓位方向：LONG;SHORT
        ranges: LONG;SHORT

content_markdown: |-
                #### **备注**

                仅供做市商使用

                #### **限流规则**

                200/s/apikey
right_code_blocks:
  - code_block: |-
      {
        "error": {
          "code": "",
          "msg": ""
        },
        "msgInfo": "success",
        "result": {
                      "createOrdersResponse": [
                        {
                          "clientOrderId": "abc123",
                          "orderId": "100001",
                          "createState": 1
                        }
                      ],
                      "cancelOrdersResponse": [
                        {
                          "cancelOrderId": "100002",
                          "cancelState": 1
                        }
                      ]      
         },
        "returnCode": 0
      }
    title: Response
    language: json
---