+++
date = '2026-09-14T15:29:44+08:00'
draft = false
title = 'DeepSeek Harness 搭配任意模型与 MCP 接入 Blender：从下载安装到提示词建模跑车全流程教程'
tags = ['blender','mcp','deepseek','dsh','ai建模','教程','uv','本地建模']
description = '相关指令请参考下面内容'
categories = ['ai相关']
+++

## 相关指令和提示词

```
# blender 下载
https://www.blender.org/download/

# blender 社区
https://www.blender.org/lab/mcp-server/

# mcp server
git clone https://projects.blender.org/lab/blender_mcp.git

# 安装uv工具
winget install --id=astral-sh.uv -e

# 检测uv版本
uv --version

# 配dsh
- insert:

    - id: mcp-blender

      name: '@deepseek-ai/dsh-mcp-client'

      config:

        serverName: blender

        transport: stdio

        command: uv

        args:

          - "--directory"

          - "C:\\你自己的目录\\blender_mcp\\mcp"

          - "run"

          - "blender-mcp"
            
  

```


```
# 提示词
请使用 Blender MCP 创建一辆现代高性能跑车。

整体采用低矮、宽体、流线型的超级跑车造型，车身比例具有明显的运动感和攻击性。

- 车身使用亮红色金属汽车漆
- 黑色碳纤维前唇、侧裙和后扩散器
- 设计锐利细长的 LED 前大灯和尾灯
- 宽大的前进气口和两侧侧进气口
- 四个大尺寸运动轮毂，黑色或深灰色
- 配备红色刹车卡钳
- 后部加入一个运动型尾翼
- 车顶和车窗使用深色玻璃
- 车身曲面要流畅、光滑，具有真实汽车的比例和结构
- 车辆左右保持对称
- 各主要部件尽量独立建模，避免明显穿模

整体效果参考现代超级跑车，强调**低趴、宽体、红色车身、黑色运动套件和强烈的视觉冲击力**。

完成后设置简单的工作室灯光和摄像机，从车辆前方 45° 角度展示整车。
```

## 视频链接

视频演示请参阅，请前往[链接]()。

---

付费咨询，远程一对一指导，请联系：gao_mygoh 。