+++
date = '2026-08-29T09:44:23+08:00'
draft = false
title = '手把手教你用 llama.cpp 本地部署 AI 大模型：从 GitHub 安装、魔搭下载 GGUF 到手机端访问，一篇讲清全流程'
tags = ['ai','llm','llama.cpp','本地部署','大模型','gguf','魔搭','教程']
description = '相关指令请参考下面内容'
categories = ['ai相关']
+++

## 相关指令

```
#查看显卡信息
nvidia-smi

#查看 llama 安装是否成功
llama-cli --version

#魔搭下载大模型
modelscope download --model Abiray/Qwen3.8-27B-Q4_K_M-GGUF Qwen3.8-27B-Q4_K_M.gguf --local_dir ./

#llama加载大模型指令
llama-server -m ./Qwen3.8-27B-Q4_K_M.gguf -c 16384 --port 8080 -ngl 999 --host 0.0.0.0

```

```
#接入deepseek harness 配置方式

provide id：llamacpp（随意输入）

api地址：http://127.0.0.1:8080/v1

密钥：123321（随意输入）
```

## 视频链接

视频演示请参阅，请前往[youtube链接](https://youtu.be/hKYQVRfARTM)。

---

付费咨询，远程一对一指导，请联系：gao_mygoh 。