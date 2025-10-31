---
title: 获取单个交易对的配置信息
position_number: 3
type: get
description: /az/future/market/v1/public/symbol/detail
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: 交易对
        ranges:
content_markdown: 注：**此方法不需要签名**
left_code_blocks:
    -
        code_block: "public void getKLine() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/az/future/market/v1/getKLine?market=btc_usdt&type=1min&since=0\");\r\n\tSystem.out.println(text);\r\n}"
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
                        "id": 110,
                        "symbol": "btc_usdt",                      //交易对
                        "symbolGroupId": 1,
                        "pair": "btc_usdt",                        //标的交易对
                        "contractType": "PERPETUAL",               //合约类型，永续，交割
                        "productType": "perpetual",                //合约类型，perpetual, futures，不区分交割间隔
                        "underlyingType": "U_BASED",               //标的类型，币本位，u本位
                        "contractSize": "0.0001",                  //合约乘数（面值）
                        "tradeSwitch": true,                       //交易对开关
                        "openSwitch": true,
                        "isDisplay": true,                         //是否展示
                        "isOpenApi": true,                         //是否支持OpenApi
                        "state": 0,                                //状态
                        "initLeverage": 20,                        //初始杠杆倍数
                        "initPositionType": "CROSSED",             //初始仓位类型
                        "baseCoin": "btc",                         //标的资产
                        "spotCoin": "BTC",
                        "quoteCoin": "usdt",                       //报价资产
                        "baseCoinPrecision": 8,                    //标的币种精度
                        "baseCoinDisplayPrecision": 5,             //标的币种显示精度
                        "quoteCoinPrecision": 8,                   //报价币种精度
                        "quoteCoinDisplayPrecision": 4,            //报价币种显示精度
                        "quantityPrecision": 0,                    //数量精度
                        "pricePrecision": 1,                       //价格精度
                        "supportOrderType": "LIMIT,MARKET",        //支持订单类型
                        "supportTimeInForce": "GTC,FOK,IOC,GTX",   //支持有效方式
                        "supportEntrustType": "TAKE_PROFIT,STOP,TAKE_PROFIT_MARKET,STOP_MARKET,TRAILING_STOP_MARKET",   //支持计划委托类型
                        "supportPositionType": "CROSSED,ISOLATED", //支持仓位类型
                        "minQty": "1",                             //最小数量
                        "minNotional": "0.1",                      //最小名义价值
                        "maxNotional": "10000000",                 //最大名义价值
                        "multiplierDown": "0.1",                   //限价卖单下限百分比
                        "multiplierUp": "0.1",                     //限价买单价格上限百分比
                        "maxOpenOrders": 20000000,                 //最多open订单
                        "maxEntrusts": 20000000,                   //最多open条件单
                        "makerFee": "0.0002",                      //maker手续费
                        "takerFee": "0.00065",                     //手续费
                        "liquidationFee": "0.015",                 //强平手续费
                        "marketTakeBound": "0.2",                  //市价单最多价格偏离
                        "depthPrecisionMerge": 6,                  //盘口精度合并
                        "labels": [],                              //标签
                        "onboardDate": 1651327201000,              //上线时间
                        "enName": "BTCUSDT",                       //合约英文名称
                        "cnName": "BTCUSDT ",                      //合约中文名称
                        "minStepPrice": "0.1",                     //最小价格变动单位
                        "deliveryDate": 1667819989000,             //交割时间
                        "deliveryCompletion": false,               //交割是否完成
                        "cnDesc": "cn btc",                        //合约中文描述
                        "enDesc": "en en",                         //合约英文描述
                        "plates": [                                //板块
                            52
                        ],
                        "fastTrackCallbackRate1": "0.01",          //跟踪委托-快捷回调率1
                        "fastTrackCallbackRate2": "0.02",          //跟踪委托-快捷回调率2
                        "minTrackCallbackRate": "0.002",           //跟踪委托-最小回调率
                        "maxTrackCallbackRate": "0.1",             //跟踪委托-最大回调率
                        "latestPriceDeviation": 0.01,              //最新价格与标记价格偏离
                        "marketOpenTakeBound": 0.005,              //市价开偏离比例
                        "marketCloseTakeBound": 0.05               //市价平偏离比例
          }
        }
      title: Response
      language: json
---