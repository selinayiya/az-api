---
title: 批量下、撤单
position_number: 8
type: post
description: /az/spot/batch-order/basket
parameters:
  - name: createOrderFirst
    type: bool
    mandatory: false
    default: true
    description: 默认下单优先，否则撤单优先
    ranges:
  - name: clientBatchId
    type: string
    mandatory: true
    default: 
    description: 批量下、撤单批次号
    ranges:
  - name: createOrders
    type: Set&lt;OrderCreateReqDTO&gt;
    mandatory: false
    default: 
    description: 下单列表，下单参数OrderCreateReqDTO集合
    ranges: 最大支持100个
  - name: cancelOrderIds
    type: Set&lt;Long&gt;
    mandatory: false
    default:
    description: 撤单列表，订单Id的集合
    ranges: 最大支持100个
      
tables:
  - title: OrderCreateReqDTO
    data:
      -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
      -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 客户端ID正则：^[a-zA-Z0-9_]{4,32}$
        ranges:
      -
        name: side
        type: string
        mandatory: true
        default:
        description: "买卖方向 \_BUY-买,SELL-卖"
        ranges:
      -
        name: type
        type: string
        mandatory: true
        default:
        description: "订单类型 \_LIMIT-限价,MARKET-市价\_"
        ranges:
      -
        name: timeInForce
        type: string
        mandatory: true
        default:
        description: 有效方式 GTC, FOK, IOC, GTX
        ranges:
      -
        name: bizType
        type: string
        mandatory: true
        default:
        description: >-
          业务类型  SPOT-现货, LEVER-杠杆
        ranges:
      -
        name: price
        type: number
        mandatory: false
        default:
        description: 价格。限价必填; 市价不填
        ranges:
      -
        name: quantity
        type: number
        mandatory: false
        default:
        description: 数量。限价必填；市价按数量下单时必填
        ranges:
      -
        name: quoteQty
        type: number
        mandatory: false
        default:
        description: 金额。限价不填；市价按金额下单时必填
        ranges:

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
        "result": [{
                      "createOrdersResponse": [
                        {
                          "clientOrderId": "abc123",
                          "orderId": "100001",
                          "createState": "ORDER_000"  //参考响应代码
                        }
                      ],
                      "cancelOrdersResponse": [
                        {
                          "cancelOrderId": "100002",
                          "cancelState": "ORDER_000" //参考响应代码
                        }
                      ]      
                  }],
        "returnCode": 0
      }
    title: Response
    language: json
---