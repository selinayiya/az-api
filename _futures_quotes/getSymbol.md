---
title: Get Configuration Information for Single Trading Pair
position_number: 3
type: get
description: /az/future/market/v1/public/symbol/detail
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: N/A
        description: Trading pair
        ranges:
content_markdown: Note：This method does not require a signature.
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
                        "symbol": "btc_usdt",                      //Trading pair
                        "symbolGroupId": 1,                                                                             
                        "pair": "btc_usdt",                        //Target trading pair
                        "contractType": "PERPETUAL",               //Contract type, perpetual, delivery
                        "productType": "perpetual",                //Contract type, perpetual, futures, regardless of delivery interval
                        "underlyingType": "U_BASED",               //Target type, Coin-M,USDT-M
                        "contractSize": "0.0001",                  //Contract multiplier(face value)
                        "tradeSwitch": true,                       //Trading pair switch
                        "openSwitch": true,
                        "isDisplay": true,                         //whether to display
                        "isOpenApi": true,                         //Whether to support OpenApi
                        "state": 0,                                //Status
                        "initLeverage": 20,                        //Initial leverage
                        "initPositionType": "CROSSED",             //Initial position type
                        "baseCoin": "btc",                         //Target Assets
                        "spotCoin": "BTC",
                        "quoteCoin": "usdt",                       //Quote currency
                        "baseCoinPrecision": 8,                    //Target currency precision
                        "baseCoinDisplayPrecision": 5,             //Displayed target currency precision
                        "quoteCoinPrecision": 8,                   //Quote currency precision
                        "quoteCoinDisplayPrecision": 4,            //Displayed quote currency precision
                        "quantityPrecision": 0,                    //Quantity precision
                        "pricePrecision": 1,                       //Price precision
                        "supportOrderType": "LIMIT,MARKET",        //Order type supported
                        "supportTimeInForce": "GTC,FOK,IOC,GTX",   //Valid ways supported
                        "supportEntrustType": "TAKE_PROFIT,STOP,TAKE_PROFIT_MARKET,STOP_MARKET,TRAILING_STOP_MARKET",   //Trigger order type supported
                        "supportPositionType": "CROSSED,ISOLATED", //Support position type
                        "minQty": "1",                             //Minimum quantity
                        "minNotional": "0.1",                      //Minimum notional value
                        "maxNotional": "10000000",                 //Maximum Notional Value
                        "multiplierDown": "0.1",                   //Floor percentage of sell limit order
                        "multiplierUp": "0.1",                     //Cap percentage of buy limit order
                        "maxOpenOrders": 20000000,                 //Maximum open orders
                        "maxEntrusts": 20000000,                   //Maximum active orders
                        "makerFee": "0.0002",                      //Maker fee
                        "takerFee": "0.00065",                     //Taker fee
                        "liquidationFee": "0.015",                 //Forced liquidation fee
                        "marketTakeBound": "0.2",                  //Market order maximum price deviation
                        "depthPrecisionMerge": 6,                  //Handicap Precision Consolidation
                        "labels": [],                              //Label
                        "onboardDate": 1651327201000,              //List time
                        "enName": "BTCUSDT",                       //Contract English name
                        "cnName": "BTCUSDT ",                      //Contract Chinese name
                        "minStepPrice": "0.1",                     //Smallest tick
                        "deliveryDate": 1667819989000,             //delivery time
                        "deliveryCompletion": false,               //Whether the delivery is completed
                        "cnDesc": "cn btc",                        //Chinese description of the contract
                        "enDesc": "en en",                         //English description of the contract
                        "plates": [
                            52
                        ],
                        "fastTrackCallbackRate1": "0.01",          //Trailing Order – Quick Callback Rate 1
                        "fastTrackCallbackRate2": "0.02",          //Trailing Order – Quick Callback Rate 2
                        "minTrackCallbackRate": "0.002",           //Trailing Order – Minimum Callback Rate
                        "maxTrackCallbackRate": "0.1",             //Trailing Order – Maximum Callback Rate
                        "latestPriceDeviation": 0.01,              //Deviation between Latest Price and Mark Price
                        "marketOpenTakeBound": 0.005,              //Market Order Opening Deviation Ratio
                        "marketCloseTakeBound": 0.05               //Market Order Closing Deviation Ratio
              }
        }
      title: Response
      language: json
---