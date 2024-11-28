---
title: "初识模型量化"
date: 2024-11-25
categories:
  - Blog
tags:
  - LLM
  - Quantization
---

# What
模型量化实际上是一种映射。
学过机器视觉的话，其实不会太陌生。

在机器视觉中经常会有将图片像素归一化的过程，将一张unit8,0~255范围的图像归一化为一个float32,0.0~1.0的张量，这就是反量化。

反过来讲float32->uint8，就叫做量化。

反量化一般没有精度损失，量化一般伴随精度损失。这不难理解，因为float32是高精，而uint8是低精。

总觉得像这样把别人的话再说一次，太蠢了，附上学习的链接：
> <cite><a href="https://zhuanlan.zhihu.com/p/149659607?utm_psn=1843396897911492608">神经网络量化入门--基本原理</a></cite>

> <cite><a href="https://www.zhihu.com/column/c_1258047709686231040">大白话模型量化</a></cite>

这是smoothquant：
> <cite><a href="https://github.com/mit-han-lab/smoothquant">smoothquant</a></cite>