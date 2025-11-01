---
title: 获取listenKey
position_number: 1.1
type: get
description: /az/future/user/v1/user/listen-key
content_markdown: |-
             注：**有效时间为8小时**
             #### **限流规则**

             200/s/apikey

left_code_blocks:
    -
        code_block: "public void getMarketConfig() {\r\n\tString text = HttpUtil.get(URL + \"/data/api/user/v1/getMarketConfig\");\r\n\tSystem.out.println(text);\r\n}"
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
          "result": "2132B8F0C778486D6EBAC39FAxxx",
          "returnCode": 0
        }
      title: Response
      language: json
---
