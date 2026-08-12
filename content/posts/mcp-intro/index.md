+++
date = '2026-08-10T10:59:44+08:00'
draft = false
title = 'AI居然能帮我薅麦当劳羊毛？MCP让AI变成你的私人助理|如何在claude中接入mcp'
tags = ['MCP','Claude MCP','MCP 教程']
description = '以下为claude桌面端的json配置项，复制之后，修改校验token可用，亲测有效'
categories = ['ai相关']
+++

## 1、不同mcp的配置json

### 12306 mcp

```
"12306-mcp": {

      "command": "npx",

      "args": [

        "-y",

        "12306-mcp"

      ]

    }
```


### 麦当劳 mcp

```
"mcd-mcp": {

      "command": "npx",

      "args": [

        "-y",

        "mcp-remote",

        "https://mcp.mcd.cn",

        "--header",

        "Authorization: Bearer 123456"

      ]

    }
```


### 高德地图 mcp

```
"amap-maps": {

      "command": "npx",

      "args": [

        "-y",

        "@amap/amap-maps-mcp-server"

      ],

      "env": {

        "AMAP_MAPS_API_KEY": "123456"

      }

    }
```

## 2、请参阅视频

[视频链接]()

---

付费咨询，远程一对一教学，请联系：gao_mygoh 。