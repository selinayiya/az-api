---
title: Batch Order Placement and Cancellation
position_number: 8
type: post
description: /az/spot/batch-order/basket
parameters:
  - name: batchCreateCancelReqDTOList
    type: Set&lt;batchCreateCancelReqDTO&gt;
    mandatory: true
    default: 
    description: 
    ranges:
      
tables:
  - title: batchCreateCancelReqDTO
    data:
      - name: createOrderFirst
        type: bool
        mandatory: false
        default: true
        description: Place orders first by default; otherwise, cancel orders first.
        ranges:
      - name: clientBatchId
        type: string
        mandatory: true
        default:
        description: Batch order request id
        ranges:
      - name: createOrders
        type: Set&lt;OrderCreateReqDTO&gt;
        mandatory: false
        default:
        description: Order list — a collection of OrderCreateDTO objects.
        ranges: Supports up to 100
      - name: cancelOrderIds
        type: Set&lt;Long&gt;
        mandatory: false
        default:
        description: Cancellation list — a collection of order IDs.
        ranges: Supports up to 100
  - title: OrderCreateReqDTO
    data:
      -
        name: symbol
        type: string
        mandatory: true
        default:
        description:
        ranges:
      -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 'Pattern: ^[a-zA-Z0-9_]{4,32}$'
        ranges:
      -
        name: side
        type: string
        mandatory: true
        default:
        description: "BUY,SELL"
        ranges:
      -
        name: type
        type: string
        mandatory: true
        default:
        description: "order type:LIMIT,MARKET"
        ranges:
      -
        name: timeInForce
        type: string
        mandatory: true
        default:
        description: effective way:GTC, FOK, IOC, GTX
        ranges:
      -
        name: bizType
        type: string
        mandatory: true
        default:
        description: "SPOT, LEVER"
        ranges:
      -
        name: price
        type: number
        mandatory: false
        default:
        description: price. Required if it is the LIMIT price; blank if it is the MARKET price
        ranges:
      -
        name: quantity
        type: number
        mandatory: false
        default:
        description: quantity. Required if it is the LIMIT price or the order is placed at the market price by quantity
        ranges:
      -
        name: quoteQty
        type: number
        mandatory: false
        default:
        description: amount. Required if it is the LIMIT price or the order is the market price when placing an order by amount
        ranges:

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
        "result": [{
                      "createOrdersResponse": [
                        {
                          "clientOrderId": "abc123",
                          "orderId": "100001",
                          "createState": "ORDER_000"  //Refer to response code
                        }
                      ],
                      "cancelOrdersResponse": [
                        {
                          "cancelOrderId": "100002",
                          "cancelState": "ORDER_000"  //Refer to response code
                        }
                      ]      
                  }],
        "returnCode": 0
      }
    title: Response
    language: json
---