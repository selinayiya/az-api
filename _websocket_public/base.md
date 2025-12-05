---
title: General WSS information
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
  
    #### **Base Address**


    **production environment: wss://s-ws.azverse.xyz/public**
    {: .info}

    **sandbox environment: wss://s-ws.myaztests.com/public**
    {: .info}


    ---


    #### **Request Headers**

    The request header of the compression extension protocol must be added.
  
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
