---
title: 公共模块
position_number: 10
parameters:
- name:
content:
content_markdown: >-
  #### **<span id="createState">Order Create State</span>**


    | State | Description |
    | --- | --- |
    | OK | Success |
    | PLATFORM_REJECT | 平台拒单 |
    | INSUFFICIENT_BALANCE | 余额不足 |
    | INSUFFICIENT_POSITION | 仓位不足 |
    | ORDER_NUMBER_LIMIT | 订单数量已达上限 |
    | LEVERAGE_MAX_QUANTITY_LIMIT | 达到杠杆数量上限 |  
    | OPEN_ORDER_PRICE_LIMIT | 触发开仓价格限制 |  
    | OPEN_ORDER_MIN_NOMINAL_VALUE_LIMIT | 触发开仓名义价值最低限制 |
    | OPEN_ORDER_MAX_NOMINAL_VALUE_LIMIT | 触发开仓名义价值最高限制 |
    | POSITION_TYPE_MISMATCH | 持仓类型不匹配 |
    | INSUFFICIENT_LEVELING_QUANTITY | 可用于平仓的数量不足 |
    | POSITION_ALREADY_LIQUIDATION | 仓位已被平仓 |
    | MARKET_DEVIATION_RISK_CONTROL | 市场偏离风险控制 |
    | OPEN_ORDER_BUY_PRICE_LIMIT | 买入价格不能超过P1（P1=标记价格 * (1 + 买单限制)） |
    | OPEN_ORDER_SELL_PRICE_LIMIT | 卖出价格不能低于P2（P2=标记价格 * (1 - 卖单限制)） |
    | RISK_USER_LIMIT_LEVERAGE | 风险用户杠杆限制 |
    | EXIST_BONUS_POSITON_NOT_CREATE_REVERSE_POSITION | 由于存在赠金仓位，无法开立反向仓位 |
    | EXIST_DEPOSIT_COUPON_NOT_CREATE_ISOLATED_ORDER | 存在充值券时，无法创建逐仓订单 |
    | MARKPRICE_INVALID | 标记价格无效，无法创建订单 |


  #### **<span id="cancelState">Order Cancel State</span>**

    | State | Description |
    | --- | --- |
    | OK | Success |
    | ORDER_CANCELED | 无效订单 |
    | PLATFORM_REJECT | 平台拒单 |



left_code_blocks:
- code_block:
  title:
  language:
  right_code_blocks:
- code_block:
  title:
  language:
---


