---
title: Public module
position_number: 10
parameters:
- name:
content:
content_markdown: >-
  #### **<span id="createState">Order Create State</span>**


    | State | Description |
    | --- | --- |
    | OK | Success |
    | PLATFORM_REJECT | Platform reject. |
    | INSUFFICIENT_BALANCE | Insufficient balance. |
    | INSUFFICIENT_POSITION | Insufficient position. |
    | ORDER_NUMBER_LIMIT | The number of orders has reached the maximum. |
    | LEVERAGE_MAX_QUANTITY_LIMIT | Leverage_max_quantity_limit. |  
    | OPEN_ORDER_PRICE_LIMIT | Open order price limit. |  
    | OPEN_ORDER_MIN_NOMINAL_VALUE_LIMIT | Minimum nominal value limit for opening orders. |
    | OPEN_ORDER_MAX_NOMINAL_VALUE_LIMIT | Maximum nominal value limit for opening orders. |
    | POSITION_TYPE_MISMATCH | Position type mismatch. |
    | INSUFFICIENT_LEVELING_QUANTITY | Insufficient leveling quantity. |
    | POSITION_ALREADY_LIQUIDATION | Position already liquidated. |
    | MARKET_DEVIATION_RISK_CONTROL | Market deviation risk control |
    | OPEN_ORDER_BUY_PRICE_LIMIT | The buy price cannot exceed P1 (P1 = mark price × (1 + buy limit)). |
    | OPEN_ORDER_SELL_PRICE_LIMIT | The sell price cannot be lower than P2 (P2 = mark price × (1 − sell limit)). |
    | RISK_USER_LIMIT_LEVERAGE | Risk user leverage limit. |
    | EXIST_BONUS_POSITON_NOT_CREATE_REVERSE_POSITION | A bonus position exists, so a reverse position cannot be created. |
    | EXIST_DEPOSIT_COUPON_NOT_CREATE_ISOLATED_ORDER | Cannot create an isolated order when a deposit coupon exists. |
    | MARKPRICE_INVALID | Invalid mark price for creating an order. |
  

  #### **<span id="cancelState">Order Cancel State</span>**

    | State | Description |
    | --- | --- |
    | OK | Success |
    | ORDER_CANCELED | Invalid order |
    | PLATFORM_REJECT | Platform Reject |
  

left_code_blocks:
- code_block:
  title:
  language:
  right_code_blocks:
- code_block:
  title:
  language:
---


