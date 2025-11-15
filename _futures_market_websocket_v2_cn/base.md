---
title: 基本信息
position_number: 1
type:
description: 

parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    #### **基地址**

    **生产环境: wss://f-ws.azverse.com/ws/market**
    {: .info}

    **测试环境: wss://f-ws.myaztests.com/ws/market**
    {: .info}


    ---


    #### **Request Headers**

    请求头必须添加压缩扩展协议。

    <font color="#aa5500">Sec-Websocket-Extensions:permessage-deflate</font>  
left_code_blocks:
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block:
        title: Response
        language: json
---
