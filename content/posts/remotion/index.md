+++
date = '2026-06-05T16:19:47+08:00'
draft = false
title = 'Remotion完全指南：用React代码生成视频的前端框架教程'
tags = ['Remotion', '视频制作', 'React', 'TypeScript', '前端开发', '视频编程', 'AI辅助开发', '代码生成视频', 'Web开发']
description = '深入了解Remotion视频框架：一个基于React的程序化视频制作工具。本教程详细讲解Remotion是什么、如何安装配置、项目结构解析，以及如何使用AI工具结合Remotion快速创建动态视频。适合前端开发者学习用代码制作专业视频。'
categories = ['ai相关']
+++

相信大家对remotion这个工具，都有一定的了解。

它可以做很多酷炫的特效素材，还可以给视频添加一些好玩的效果。

有些人会认为，这是ai工具，或者这是一个大模型。

其实，这些认知都是错误。

今天这个视频，我从根上带大家梳理一下这个工具。

看完这个视频之后，你对remotion会有一个更加清晰的认识，自然就会知道该怎么对remotion这个项目进行增删改查了。

并且我会分享更加简单、更加快捷的方法，让你也能用remotion做出视频。

你不需要安装codex、claude code，你只要手头有 vscode、cursor 这些编程工具就可以了。

## 1、remotion 是什么

有些朋友可能会认为，remotion 是一个 ai 工具。类似于 claude code，codex……

还有些朋友可能会认为，它是一个模型，可以直接通过提示词生成视频。类似，seedance，sora模型。

这个观点是错误的。

它跟ai上是没有关系的。

假如说，我们时光倒流了，回到5、6年前，没有ai，那么remotion……

我们依然可以手写代码，使用remotion框架来生成视频。


它是一个代码开发的框架，借助H5、 CSS、Canvas、SVG、WebGL 等前端技术，将图形、文字、图片等元素，通过浏览器渲染出来，让用户看到动态效果，最后，再把这些动态效果，转化为视频。

remotion 不能凭空，生成一个猫……

它只能基于现有的素材，进行变化……

其实，它更像是ppt。

大家仔细理解一下，好好揣摩揣摩。

那为什么它在ai赛道这么火爆呢？

因为，ai可以写代码，代码可以通过remotion框架生成视频。所以，它火了。

## 2、remotion 项目介绍

我们先找一个空的文件夹，把remotion项目放到这里。

检查你的node版本是否 >= 20。

没有安装node的朋友，建议使用nvm工具进行安装，由于过于简单，我们就不多说了。

打开官网，复制粘贴指令。

```
npx create-video@latest
```

找到一个合适的文件夹，打开终端，输入指令。

一路选择默认就可以了。

使用vscode……

npm i 下载……

npm run dev 打开……studio 工作站。

此刻，我们看到的一个空的项目，视频后面，我会分享怎么使用它。

项目的根目录下，我们看到有很多文件，我们看到有很多熟悉的……claude ，codex，cursor

如果出现报错，请在命令行输入以下指令，配置代理

```
$env:HTTP_PROXY="http://127.0.0.1:10808"
$env:HTTPS_PROXY="http://127.0.0.1:10808" 
```

这些都是各种 **AI 编程助手/IDE** 的配置文件夹，每个对应一款不同的工具：

| 文件夹 | 对应工具 |
|--------|----------|
| .agent / .agents | VS Code Copilot Agent / 通用 agent 配置 |
| .claude | [Claude Code](https://claude.ai/code)（Anthropic） |
| .cline | [Cline](https://github.com/cline/cline)（VS Code 插件） |
| .codex | [OpenAI Codex CLI](https://github.com/openai/codex) |
| .cursor | [Cursor](https://cursor.sh/)（AI IDE） |
| .windsurf | [Windsurf](https://codeium.com/windsurf)（Codeium 的 AI IDE） |
| .continue | [Continue](https://continue.dev/)（VS Code 插件） |
| .gemini | [Gemini CLI](https://github.com/google-gemini/gemini-cli)（Google） |
| .roo | [Roo Code](https://roocode.com/)（VS Code 插件） |
| .trae | [Trae](https://www.trae.ai/)（字节跳动 AI IDE） |
| .goose | [Goose](https://github.com/block/goose)（Block/Square） |
| .openhands | [OpenHands](https://github.com/All-Hands-AI/OpenHands)（原 OpenDevin） |
| .kiro | [Kiro](https://kiro.dev/)（AWS） |
| .qwen | 通义千问相关工具 |
| .mcpjam | MCP（Model Context Protocol）相关工具 |
| .factory | [Factory](https://www.factory.ai/) |
| .crush / .pi / .pochi 等 | 其他 AI 编程工具 |


其它目录：


public - 存放公共资源（比方说，加工的视频，图片等等）；

skills - skill的总目录，它是remotion官方维护的skill……其它 ai 工具下的skill，文件结构一样……其它ai工具下的skill 是副本……

src — 主要源码（视频通过这些代码制作出来）；

其它的文件主要是配置相关的文件，以及项目说明文件。

接下来聊一下如何使用。

## 3、remotion使用

使用vscode的ai插件，输入提示词，生成视频。

```
你是一个精通 React、TypeScript 和最新版 Remotion 视频框架的顶级 Motion Designer。
我需要你编写一个 15 秒（fps=30，共 450 帧）、分辨率为 1920x1080 的科技感 AI 主题视频。

【主题】
《AI 代理演进史：从 Prompt 到自主 Agent》

【视频结构与分镜】
1. 0 - 3 秒（0-90帧）：【前言：数据奇点】
   - 背景：深黑色 canvas，带有逐渐亮起的动态科技网格（使用 SVG 绘制）。
   - 动画：居中显示大标题“AI AGENTS”，字母间距由散开逐渐收拢，并伴随模糊（blur）渐变消退的效果。
2. 3 - 8 秒（90-240帧）：【进化：从 Prompt 到智能化】
   - 画面左侧：展示一段打字机效果的代码流（模拟 Prompt 交互），文字逐字蹦出。
   - 画面右侧：一个 3D 质感的圆形粒子球（使用 CSS 或 Canvas），随着“代码”的输入，粒子球的半径、旋转速度和颜色（从冷蓝到极光紫）发生明显的“激活”变化。
3. 8 - 13 秒（240-390帧）：【多 Agent 协作网络】
   - 核心效果：画面中央展开一个包含 3 个节点的拓扑图（AI 主控、数据分析、代码执行）。
   - 动画：节点与节点之间有发光的数据流线条（Dash-offset 动画）在快速穿梭。各节点伴随弹簧动画（spring）依次放大并产生呼吸光晕。
4. 13 - 15 秒（390-450帧）：【片尾：未来已来】
   - 画面淡出：背景网格亮度降低。
   - 结算特效：一个科技感十足的进度条（0% 飞速加载到 100%），上方浮现文案 “The Future is Programmatic.”。

【必须体现的 Remotion 核心用法与高级技术指标】
- 使用  绝对定位构建多层画布。
- 必须使用  精准控制上述 4 个分镜的入场、出场和时间重叠。
- 严禁硬编码（Hardcode）动画数值。所有动画必须由 `useCurrentFrame()` 驱动。
- 运用 `interpolate` 实现复合属性联动，例如将 frame 映射到：opacity [0 to 1], scale [0.5 to 1], filter [blur(10px) to blur(0px)]。
- 运用 `spring` 物理引擎函数（设置 config: { damping: 12, mass: 0.5 }），为节点诞生、弹窗弹出赋予极度丝滑的 Q 弹果冻感动画。
- 所有非本地资源（若用到网络图片或字体）必须使用 Remotion 内置的 `` 组件，防止渲染时出现首帧闪烁。
- 代码结构清晰，将各个分镜抽象为独立的子组件，并使用 TypeScript 规范定义 Props 接口以体现 Remotion 的可复用性和参数化（Parameterized）特性。
```

添加进度条

```
我在public里面增加了一个视频，请帮我制作章节进度条，进度条在视频上方。

第一章: 0 - 1:10，入门介绍；

第二章: 1:10-2:30，高级介绍；

第三章: 2:30-4:00，实战；

第四章:4:00-结尾，总结。
```

……导出，你会发现时间特别长。




单独做进度条。

```
我希望制作一个视频的进度条，视频的总时长为4分钟。目前，还没有这个视频。请先将进度条做出来。

信息如下：

第一章: 0 - 1:10，项目介绍；

第二章: 1:10-2:30，基础操作；

第三章: 2:30-4:00，实战；
```

这个导出的时间，就相对少了很多……

后面，我们将这一段视频放在副轨道上，然后将其它部分遮住就可以了。


最后，我们看一下这个视频项目的管理，看完之后，你会对 remotion 这个工具，有更清晰地把握。

启动工作台之后，我们看到 assets，assets 是资产的意思，对应着public目录下的内容。

可以点击这里打开目录……添加文件……

compositions 是作品的意思，工作台这里我们通过点击可以看到刚才创建的作品。

而在src目录下，我们可以看到同名的代码文件，没错，这些动效，是通过这些代码创建出来的。

而这些代码又全部注册在了root这个代码文件下。这个写法，是 remotion 这个框架规定。

只要有一个新视频，就会在root中，创建一个 composition 组件，并且也会生成一个新的代码源文件。

这就是视频与代码的对应关系。假如说，你对这个视频不满意……

如果你想删除文件，点击……

你会看到，它对应代码，以及root文件中的组件也都没有了。

如果整个项目，你都不想要了，那就直接删除好了，然后，重新输入指令，起一个项目 —— 清清爽爽，不留一丝痕迹。万花丛中过，片叶不沾身。

-------------

相信大家看完本期视频之后，对remotion有更清晰的认识。

并且可以借助 ai 做一些简单的视频。

时间有限，关于这个工具的配置项内容，还有如何结合 codex 做视频的内容，还没有具体讲。

后面本频道会继续出视频，跟大家分享更多remotion相关的内容。

ok，以上就是本期分享……



