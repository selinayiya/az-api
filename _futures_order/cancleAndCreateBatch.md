---
title: Batch Order Placement and Cancellation
position_number: 8
type: post
description: /az/future/trade/v1/order/batch
remark: Content-Type = application/x-www-form-urlencoded && application/json
parameters:
  - name: createOrderFirst
    type: bool
    mandatory: false
    default: true
    description: Place orders first by default; otherwise, cancel orders first.
    ranges:
  - name: createOrders
    type: Set&lt;OrderCreateDTO&gt;
    mandatory: false
    default: 
    description:  Order list — a collection of OrderCreateDTO objects.
    ranges: Supports up to 100
  - name: cancelOrderIds
    type: Set&lt;Long&gt;
    mandatory: false
    default:
    description: Cancellation list — a collection of order IDs.
    ranges: Supports up to 100
      
tables:
  - title: OrderCreateDTO
    data:
      -
        name: clientOrderId
        type: string
        mandatory: true
        default: N/A
        description: Client order ID
        ranges: 
      -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair
        ranges:
      -
        name: orderSide
        type: string
        mandatory: true
        default: N/A
        description: Order side:BUY;SELL
        ranges: BUY;SELL
      -
        name: orderType
        type: string
        mandatory: true
        default: N/A
        description: Order type:LIMIT；MARKET
        ranges: LIMIT；MARKET
      -
        name: origQty
        type: number
        mandatory: true
        default: N/A
        description: Quantity (Cont)
        ranges:
      -
        name: price
        type: number
        mandatory: false
        default: N/A
        description: Price
        ranges:
      -
        name: timeInForce
        type: string
        mandatory: false
        default: GTC
        description: Valid way:GTC;IOC;FOK;GTX
        ranges: GTC;IOC;FOK;GTX
      -
        name: triggerProfitPrice
        type: number
        mandatory: false
        default: N/A
        description: Stop profit price
        ranges:
      -
        name: triggerStopPrice
        type: number
        mandatory: false
        default: N/A
        description: Stop loss price
        ranges:
      -
        name: positionSide
        type: string
        mandatory: true
        default: N/A
        description: Position side:LONG;SHORT
        ranges: LONG;SHORT

content_markdown: |-
                #### **Note**

                For Market Makers Only


                #### **Limit Flow Rules**

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
                          "orderId": 100001,
                          "createState": 1
                        }
                      ],
                      "cancelOrdersResponse": [
                        {
                          "cancelOrderId": 100002,
                          "cancelState": 1
                        }
                      ] 
        },
        "returnCode": 0
      }
    title: Response
    language: json
---