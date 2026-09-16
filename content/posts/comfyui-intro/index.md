+++
date = '2026-09-16T21:18:04+08:00'
draft = false
title = '手把手跟着做：ComfyUI 安装创建实例、加载官方模板并跑通 MiniMax H3 图生视频工作流'
tags = ['comfyui','minimax h3','aigc','huggingface','unet','魔搭','图生视频','教程']
description = '相关指令请参考下面内容'
categories = ['ai相关']
+++

## 相关指令

```
# 下载 hugging face 客户端
python -m pip install -U huggingface_hub

#一定要输入下面这个指令，配置镜像，否则会下载失败
$env:HF_ENDPOINT="https://hf-mirror.com"

#复制刚才的链接 加上 --local-dir ./ 表示下载到当前这个文件夹
hf download hf://Comfy-Org/MiniMax-H3/diffusion_models/minimax_h3_fl2va_pruned_int8_convrot.safetensors --local-dir ./

# 下载魔搭客户端
python -m pip install -U modelscope


# 下载大模型
modelscope download --model Comfy-Org/MiniMax-H3 diffusion_models/minimax_h3_fl2va_pruned_int8_convrot.safetensors --local_dir ./
```

## 视频链接

视频演示请参阅，请前往[链接]()。

---

付费咨询，远程一对一指导，请联系：gao_mygoh 。