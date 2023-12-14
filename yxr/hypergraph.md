---
title: 超图
description: 
published: true
date: 2023-12-14T07:43:14.880Z
tags: hypergraph
editor: markdown
dateCreated: 2023-12-13T06:51:45.763Z
---

# HyperGraph

## 超图模型的构建

<img src='/hypergraph/超图模型.png' width=100%>

当处理图像识别任务时，每个顶点表示图像像素。

当处理图像检索任务时，每个顶点表示目标域。

<img src='/hypergraph/超图lib.png' width=100%>

> Q:如何对一个图像构造超图
> E:


### 4D Light Field Segmentation From Light Field Super-Pixel Hypergraph Representation

旨在使用超图完成4D光场分割任务。
为了减少计算量，对图像进行了粗化处理。

顶点为标记的图像块、未标记的图像块和分块的种类
超边连接了标记的图像块和每个块种类（距离0或去除该超边），未标记的图像块和每个块种类，标记的图像块和未标记的图像块（满足定义的邻域关系）

使用图割法最小化能量函数划分。

在非朗伯场景的分割效果不理想。