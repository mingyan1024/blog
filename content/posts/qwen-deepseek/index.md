+++
date = '2026-08-18T15:30:47+08:00'
draft = false
title = '不用买Token！本地部署千问3.8，免费接入DeepSeek Harness｜AI大模型本地运行教程'
tags = ['DeepSeek Harness','Qwen3.8','千问3.8','本地部署大模型','llama.cpp','AI Agent','本地AI']
description = 'deepseek harness 接入千问3.8大模型，相关指令汇总'
categories = ['AI相关']
+++

## 1、相关指令

### 显卡信息

```
nvidia-smi
```
### llama 版本确认

```
llama-cli --version
```

### hugging face 大模型下载

```
$env:HF_ENDPOINT="https://hf-mirror.com"
hf download hf://unsloth/Qwen3.8-27B-GGUF/Qwen3.8-27B-UD-Q4_K_XL.gguf  --local-dir ./
```

### 大模型加载

```
llama-server -m ".\Qwen3.8-27B-UD-Q4_K_XL.gguf" -ngl 999 
```

### 大模型体检

```
http://127.0.0.1:8080/health
```

### 接入deepseek harness配置

```
qwen

qwen-local

http://127.0.0.1:8080/v1

密钥随意输入
```

## 2、视频链接

请参照视频操作，[视频链接](https://youtu.be/Sk_bp9Dq9Ik)。

---

付费咨询，远程一对一指导，请联系：gao_mygoh 。